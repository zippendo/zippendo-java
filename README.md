# Zippendo Java SDK

Official Java client for the [Zippendo](https://zippendo.com) shipping & logistics API. Built on
`java.net.http` and Jackson, so it adds no HTTP library to your classpath. Requires Java 11+.

Book shipments and print labels with PostNord, GLS, DAO, Bring, DHL, DPD, UPS and more, track
parcels, and manage orders, shipping rules and webhooks from your own code. New to the API? Start with
the [SDK guide](https://www.zippendo.com/docs/sdks/overview) or browse the
[API reference](https://www.zippendo.com/docs/api-reference/overview). To work from an AI assistant
instead, connect the [Zippendo MCP server](https://www.zippendo.com/docs/mcp/overview).

## Install

Maven:

```xml
<dependency>
  <groupId>com.zippendo</groupId>
  <artifactId>zippendo-java</artifactId>
  <version>1.x.y</version>
</dependency>
```

Gradle:

```kotlin
implementation("com.zippendo:zippendo-java:1.x.y")
```

Use the latest version on [Maven Central](https://central.sonatype.com/artifact/com.zippendo/zippendo-java).

## Authentication

Create an API token in your Zippendo dashboard (**Settings → API tokens**). It is a Bearer token
prefixed with `zipp_`. The client sends it from a request interceptor, which runs on every call:

```java
import com.zippendo.sdk.ApiClient;

String token = System.getenv("ZIPPENDO_API_TOKEN");

ApiClient client = new ApiClient();
client.setRequestInterceptor(request -> request.header("Authorization", "Bearer " + token));
```

The base URL defaults to `https://api.zippendo.com` — you don't need to set it.
`setRequestInterceptor` replaces any earlier interceptor, so set every default header in the same one
(see [Brands](#brands)).

## Resources & clients

The API is split into resource clients — `ShipmentsApi`, `OrdersApi`, `CarriersApi`, `AddressesApi`,
`RulesApi`, `WebhooksApi`, `TokensApi`, and more. Construct the ones you need with your `client`:

```java
import com.zippendo.sdk.api.OrdersApi;
import com.zippendo.sdk.api.ShipmentsApi;

ShipmentsApi shipments = new ShipmentsApi(client);
OrdersApi orders = new OrdersApi(client);
```

Every operation takes a request object built with `newBuilder()`, so optional filters are named
rather than positional. Each also has a positional overload.

## The `orgId` parameter

Every call takes an `orgId` (your organization ID, found in the dashboard). It is explicit on each
call by design: one API token can be granted access to multiple organizations, and `orgId` selects
which one the request acts on.

## Brands

A brand is a sub-account inside an organization: one company running several consumer-facing labels
(say Acme and Globex) keeps each label's orders and shipments separate, with its own company name,
address and logo on the documents its shipments produce. Scope a request to one brand with the
`X-Zippendo-Brand` header, whose value is the brand's ID or slug.

The header is not a method parameter — it applies uniformly to every operation, so set it in the
client's interceptor and every call made with that client inherits it:

```java
ApiClient acme = new ApiClient();
acme.setRequestInterceptor(request -> request
    .header("Authorization", "Bearer " + token)
    .header("X-Zippendo-Brand", "acme")); // brand ID or slug

new ShipmentsApi(acme).listShipments(ShipmentsApi.APIListShipmentsRequest.newBuilder()
    .orgId("org_8f3kd92ld0")
    .limit(50)
    .build()); // Acme's shipments only
```

To address two brands from one process, build an `ApiClient` per brand. For a single call, every
operation also has an overload that takes extra headers:

```java
shipments.listShipments(request, Map.of("X-Zippendo-Brand", "globex"));
```

Omit the header and the request covers the whole organization — the behaviour of every existing token.
A header naming a brand that does not exist in the organization is rejected with `404 BRAND_NOT_FOUND`.

An API token created with a `brandId` is permanently confined to that brand and needs no header.
Sending `X-Zippendo-Brand` naming a *different* brand on such a token is refused with
`403 BRAND_ACCESS_DENIED` — the binding is never widened.

List operations also take a `brandScope` parameter (`"own"` / `"shared"` / `"both"`) to narrow
further within whichever brand context already applies: `"own"` returns only that brand's rows and
needs a brand context (otherwise `400`); `"shared"` returns only the unassigned rows (equivalent to
`brandId("none")`). Add an `X-Zippendo-Brand-Scope` header to the interceptor to cover every call.
An explicit `brandScope` passed to a call still wins over the header.

### Managing brands

Brands are managed with `BrandsApi`, built from your organization-wide client, not a brand-scoped one
— you are administering brands, not acting inside one:

```java
import com.zippendo.sdk.api.BrandsApi;
import com.zippendo.sdk.model.CreateOrgBrandRequest;

BrandsApi brands = new BrandsApi(client);

var created = brands.createOrgBrand(BrandsApi.APICreateOrgBrandRequest.newBuilder()
    .orgId("org_8f3kd92ld0")
    .createOrgBrandRequest(new CreateOrgBrandRequest().name("Acme").companyName("Acme ApS"))
    .build());

brands.archiveOrgBrand(BrandsApi.APIArchiveOrgBrandRequest.newBuilder()
    .orgId("org_8f3kd92ld0")
    .brandId(created.getId())
    .build());
```

Retire a brand with `archiveOrgBrand` — archived brands keep their slug and can be restored with
`unarchiveOrgBrand`. Permanent deletion is dashboard-only: it is refused while any order, shipment,
member or token still references the brand. Brands require a plan that includes them; creating one
past your plan's limit returns `403`.

## Listing & pagination

List endpoints accept `page` (1-based) and `limit`, and return a page with `data` plus
`total`, `page`, `limit`, and `totalPages`:

```java
import com.zippendo.sdk.model.ListShipments200Response;

ListShipments200Response page = shipments.listShipments(ShipmentsApi.APIListShipmentsRequest.newBuilder()
    .orgId("org_8f3kd92ld0")
    .page(1)
    .limit(50)
    .build());

page.getData();                                    // List<ListShipments200ResponseDataInner>
System.out.println(page.getTotal() + " / " + page.getTotalPages());
```

## Creating resources

```java
import com.zippendo.sdk.model.CreateOrderRequest;
import com.zippendo.sdk.model.CreateOrderRequestOrderLinesInner;

var order = orders.createOrder(OrdersApi.APICreateOrderRequest.newBuilder()
    .orgId("org_8f3kd92ld0")
    .createOrderRequest(new CreateOrderRequest()
        .orderNumber("1001")
        .orderChannelId("chan_7d2k1")
        .addOrderLinesItem(new CreateOrderRequestOrderLinesInner().name("T-shirt").quantity(2)))
    .build());
System.out.println(order.getId());
```

See [`./docs`](./docs) for the full request/response shape of every operation.

## Error handling

Non-2xx responses throw `ApiException`. The body is Zippendo's canonical `{ code, error, message }` —
branch on the machine-readable `code`:

```java
import com.fasterxml.jackson.databind.JsonNode;
import com.zippendo.sdk.ApiException;

try {
  shipments.getShipment(ShipmentsApi.APIGetShipmentRequest.newBuilder()
      .orgId("org_8f3kd92ld0")
      .shipmentId("shp_missing")
      .build());
} catch (ApiException e) {
  JsonNode body = client.getObjectMapper().readTree(e.getResponseBody());
  System.err.println(e.getCode() + " " + body.path("code").asText()); // e.g. "404 SHIPMENT_NOT_FOUND"
}
```

## Configuration

Point the client at a different environment, or change its timeouts:

```java
client.updateBaseUri("https://staging.api.zippendo.com");
client.setReadTimeout(java.time.Duration.ofSeconds(30));
```

## Reference

Full per-endpoint and per-model documentation is in [`./docs`](./docs). Hosted reference:
<https://www.zippendo.com/docs/api-reference/overview>.

## License

[MIT](./LICENSE.md)
