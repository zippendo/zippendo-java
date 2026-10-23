# OrdersApi

All URIs are relative to *https://api.zippendo.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**createOrder**](OrdersApi.md#createOrder) | **POST** /orgs/{orgId}/orders | Create order |
| [**createOrderWithHttpInfo**](OrdersApi.md#createOrderWithHttpInfo) | **POST** /orgs/{orgId}/orders | Create order |
| [**deleteOrder**](OrdersApi.md#deleteOrder) | **DELETE** /orgs/{orgId}/orders/{orderId} | Delete order |
| [**deleteOrderWithHttpInfo**](OrdersApi.md#deleteOrderWithHttpInfo) | **DELETE** /orgs/{orgId}/orders/{orderId} | Delete order |
| [**getOrder**](OrdersApi.md#getOrder) | **GET** /orgs/{orgId}/orders/{orderId} | Get order |
| [**getOrderWithHttpInfo**](OrdersApi.md#getOrderWithHttpInfo) | **GET** /orgs/{orgId}/orders/{orderId} | Get order |
| [**listOrders**](OrdersApi.md#listOrders) | **GET** /orgs/{orgId}/orders | List orders |
| [**listOrdersWithHttpInfo**](OrdersApi.md#listOrdersWithHttpInfo) | **GET** /orgs/{orgId}/orders | List orders |
| [**updateOrder**](OrdersApi.md#updateOrder) | **PATCH** /orgs/{orgId}/orders/{orderId} | Update order |
| [**updateOrderWithHttpInfo**](OrdersApi.md#updateOrderWithHttpInfo) | **PATCH** /orgs/{orgId}/orders/{orderId} | Update order |



## createOrder

> CreateOrder201Response createOrder(createOrderRequest)

Create order

Creates a new order under an existing order channel for the organization.

### Example

```java
// Import classes:
import com.zippendo.sdk.ApiClient;
import com.zippendo.sdk.ApiException;
import com.zippendo.sdk.Configuration;
import com.zippendo.sdk.auth.*;
import com.zippendo.sdk.models.*;
import com.zippendo.sdk.api.OrdersApi;
import com.zippendo.sdk.api.OrdersApi.*;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.zippendo.com");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        OrdersApi apiInstance = new OrdersApi(defaultClient);
        String orgId = "org_8f3kd92ld0"; // String | Organization ID
        CreateOrderRequest createOrderRequest = new CreateOrderRequest(); // CreateOrderRequest | 
        try {
            APIcreateOrderRequest request = APIcreateOrderRequest.newBuilder()
                .orgId(orgId)
                .createOrderRequest(createOrderRequest)
                .build();
            CreateOrder201Response result = apiInstance.createOrder(request);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling OrdersApi#createOrder");
            System.err.println("Status code: " + e.getCode());
            System.err.println("Reason: " + e.getResponseBody());
            System.err.println("Response headers: " + e.getResponseHeaders());
            e.printStackTrace();
        }
    }
}
```

### Parameters

|    Name      |    Type       | Description   |     Notes    |
|------------- | ------------- | ------------- | -------------|
| createOrderRequest | [**APIcreateOrderRequest**](OrdersApi.md#APIcreateOrderRequest)|-|-|

### Return type

[**CreateOrder201Response**](CreateOrder201Response.md)


### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Default Response |  -  |
| **400** | Default Response |  -  |
| **403** | Default Response |  -  |
| **404** | Default Response |  -  |
| **409** | Default Response |  -  |

## createOrderWithHttpInfo

> ApiResponse<CreateOrder201Response> createOrderWithHttpInfo(createOrderRequest)

Create order

Creates a new order under an existing order channel for the organization.

### Example

```java
// Import classes:
import com.zippendo.sdk.ApiClient;
import com.zippendo.sdk.ApiException;
import com.zippendo.sdk.ApiResponse;
import com.zippendo.sdk.Configuration;
import com.zippendo.sdk.auth.*;
import com.zippendo.sdk.models.*;
import com.zippendo.sdk.api.OrdersApi;
import com.zippendo.sdk.api.OrdersApi.*;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.zippendo.com");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        OrdersApi apiInstance = new OrdersApi(defaultClient);
        String orgId = "org_8f3kd92ld0"; // String | Organization ID
        CreateOrderRequest createOrderRequest = new CreateOrderRequest(); // CreateOrderRequest | 
        try {
            APIcreateOrderRequest request = APIcreateOrderRequest.newBuilder()
                .orgId(orgId)
                .createOrderRequest(createOrderRequest)
                .build();
            ApiResponse<CreateOrder201Response> response = apiInstance.createOrderWithHttpInfo(request);
            System.out.println("Status code: " + response.getStatusCode());
            System.out.println("Response headers: " + response.getHeaders());
            System.out.println("Response body: " + response.getData());
        } catch (ApiException e) {
            System.err.println("Exception when calling OrdersApi#createOrder");
            System.err.println("Status code: " + e.getCode());
            System.err.println("Response headers: " + e.getResponseHeaders());
            System.err.println("Reason: " + e.getResponseBody());
            e.printStackTrace();
        }
    }
}
```

### Parameters

|    Name      |    Type       | Description   |     Notes    |
|------------- | ------------- | ------------- | -------------|
| createOrderRequest | [**APIcreateOrderRequest**](OrdersApi.md#APIcreateOrderRequest)|-|-|

### Return type

ApiResponse<[**CreateOrder201Response**](CreateOrder201Response.md)>


### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Default Response |  -  |
| **400** | Default Response |  -  |
| **403** | Default Response |  -  |
| **404** | Default Response |  -  |
| **409** | Default Response |  -  |


<a id="APIcreateOrderRequest"></a>
## APIcreateOrderRequest
### Properties

|     Name      |    Type       | Description   |     Notes    |
| ------------- | ------------- | ------------- | -------------|
| **orgId** | **String** | Organization ID | |
| **createOrderRequest** | [**CreateOrderRequest**](CreateOrderRequest.md) |  | |



## deleteOrder

> RevokeApiToken200Response deleteOrder(deleteOrderRequest)

Delete order

Deletes an order. Fails if the order has associated shipments.

### Example

```java
// Import classes:
import com.zippendo.sdk.ApiClient;
import com.zippendo.sdk.ApiException;
import com.zippendo.sdk.Configuration;
import com.zippendo.sdk.auth.*;
import com.zippendo.sdk.models.*;
import com.zippendo.sdk.api.OrdersApi;
import com.zippendo.sdk.api.OrdersApi.*;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.zippendo.com");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        OrdersApi apiInstance = new OrdersApi(defaultClient);
        String orgId = "clz9k2f0a0000abcd0000zzzz"; // String | Organization ID.
        String orderId = "clz9k2f0a0003abcd9012mnop"; // String | Order ID.
        try {
            APIdeleteOrderRequest request = APIdeleteOrderRequest.newBuilder()
                .orgId(orgId)
                .orderId(orderId)
                .build();
            RevokeApiToken200Response result = apiInstance.deleteOrder(request);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling OrdersApi#deleteOrder");
            System.err.println("Status code: " + e.getCode());
            System.err.println("Reason: " + e.getResponseBody());
            System.err.println("Response headers: " + e.getResponseHeaders());
            e.printStackTrace();
        }
    }
}
```

### Parameters

|    Name      |    Type       | Description   |     Notes    |
|------------- | ------------- | ------------- | -------------|
| deleteOrderRequest | [**APIdeleteOrderRequest**](OrdersApi.md#APIdeleteOrderRequest)|-|-|

### Return type

[**RevokeApiToken200Response**](RevokeApiToken200Response.md)


### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Default Response |  -  |
| **400** | Default Response |  -  |
| **403** | Default Response |  -  |
| **404** | Default Response |  -  |

## deleteOrderWithHttpInfo

> ApiResponse<RevokeApiToken200Response> deleteOrderWithHttpInfo(deleteOrderRequest)

Delete order

Deletes an order. Fails if the order has associated shipments.

### Example

```java
// Import classes:
import com.zippendo.sdk.ApiClient;
import com.zippendo.sdk.ApiException;
import com.zippendo.sdk.ApiResponse;
import com.zippendo.sdk.Configuration;
import com.zippendo.sdk.auth.*;
import com.zippendo.sdk.models.*;
import com.zippendo.sdk.api.OrdersApi;
import com.zippendo.sdk.api.OrdersApi.*;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.zippendo.com");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        OrdersApi apiInstance = new OrdersApi(defaultClient);
        String orgId = "clz9k2f0a0000abcd0000zzzz"; // String | Organization ID.
        String orderId = "clz9k2f0a0003abcd9012mnop"; // String | Order ID.
        try {
            APIdeleteOrderRequest request = APIdeleteOrderRequest.newBuilder()
                .orgId(orgId)
                .orderId(orderId)
                .build();
            ApiResponse<RevokeApiToken200Response> response = apiInstance.deleteOrderWithHttpInfo(request);
            System.out.println("Status code: " + response.getStatusCode());
            System.out.println("Response headers: " + response.getHeaders());
            System.out.println("Response body: " + response.getData());
        } catch (ApiException e) {
            System.err.println("Exception when calling OrdersApi#deleteOrder");
            System.err.println("Status code: " + e.getCode());
            System.err.println("Response headers: " + e.getResponseHeaders());
            System.err.println("Reason: " + e.getResponseBody());
            e.printStackTrace();
        }
    }
}
```

### Parameters

|    Name      |    Type       | Description   |     Notes    |
|------------- | ------------- | ------------- | -------------|
| deleteOrderRequest | [**APIdeleteOrderRequest**](OrdersApi.md#APIdeleteOrderRequest)|-|-|

### Return type

ApiResponse<[**RevokeApiToken200Response**](RevokeApiToken200Response.md)>


### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Default Response |  -  |
| **400** | Default Response |  -  |
| **403** | Default Response |  -  |
| **404** | Default Response |  -  |


<a id="APIdeleteOrderRequest"></a>
## APIdeleteOrderRequest
### Properties

|     Name      |    Type       | Description   |     Notes    |
| ------------- | ------------- | ------------- | -------------|
| **orgId** | **String** | Organization ID. | |
| **orderId** | **String** | Order ID. | |



## getOrder

> GetOrder200Response getOrder(getOrderRequest)

Get order

Returns a single order with its channel, shipping rule, shipments, and documents.

### Example

```java
// Import classes:
import com.zippendo.sdk.ApiClient;
import com.zippendo.sdk.ApiException;
import com.zippendo.sdk.Configuration;
import com.zippendo.sdk.auth.*;
import com.zippendo.sdk.models.*;
import com.zippendo.sdk.api.OrdersApi;
import com.zippendo.sdk.api.OrdersApi.*;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.zippendo.com");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        OrdersApi apiInstance = new OrdersApi(defaultClient);
        String orgId = "clz9k2f0a0000abcd0000zzzz"; // String | Organization ID.
        String orderId = "clz9k2f0a0003abcd9012mnop"; // String | Order ID.
        try {
            APIgetOrderRequest request = APIgetOrderRequest.newBuilder()
                .orgId(orgId)
                .orderId(orderId)
                .build();
            GetOrder200Response result = apiInstance.getOrder(request);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling OrdersApi#getOrder");
            System.err.println("Status code: " + e.getCode());
            System.err.println("Reason: " + e.getResponseBody());
            System.err.println("Response headers: " + e.getResponseHeaders());
            e.printStackTrace();
        }
    }
}
```

### Parameters

|    Name      |    Type       | Description   |     Notes    |
|------------- | ------------- | ------------- | -------------|
| getOrderRequest | [**APIgetOrderRequest**](OrdersApi.md#APIgetOrderRequest)|-|-|

### Return type

[**GetOrder200Response**](GetOrder200Response.md)


### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Default Response |  -  |
| **403** | Default Response |  -  |
| **404** | Default Response |  -  |

## getOrderWithHttpInfo

> ApiResponse<GetOrder200Response> getOrderWithHttpInfo(getOrderRequest)

Get order

Returns a single order with its channel, shipping rule, shipments, and documents.

### Example

```java
// Import classes:
import com.zippendo.sdk.ApiClient;
import com.zippendo.sdk.ApiException;
import com.zippendo.sdk.ApiResponse;
import com.zippendo.sdk.Configuration;
import com.zippendo.sdk.auth.*;
import com.zippendo.sdk.models.*;
import com.zippendo.sdk.api.OrdersApi;
import com.zippendo.sdk.api.OrdersApi.*;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.zippendo.com");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        OrdersApi apiInstance = new OrdersApi(defaultClient);
        String orgId = "clz9k2f0a0000abcd0000zzzz"; // String | Organization ID.
        String orderId = "clz9k2f0a0003abcd9012mnop"; // String | Order ID.
        try {
            APIgetOrderRequest request = APIgetOrderRequest.newBuilder()
                .orgId(orgId)
                .orderId(orderId)
                .build();
            ApiResponse<GetOrder200Response> response = apiInstance.getOrderWithHttpInfo(request);
            System.out.println("Status code: " + response.getStatusCode());
            System.out.println("Response headers: " + response.getHeaders());
            System.out.println("Response body: " + response.getData());
        } catch (ApiException e) {
            System.err.println("Exception when calling OrdersApi#getOrder");
            System.err.println("Status code: " + e.getCode());
            System.err.println("Response headers: " + e.getResponseHeaders());
            System.err.println("Reason: " + e.getResponseBody());
            e.printStackTrace();
        }
    }
}
```

### Parameters

|    Name      |    Type       | Description   |     Notes    |
|------------- | ------------- | ------------- | -------------|
| getOrderRequest | [**APIgetOrderRequest**](OrdersApi.md#APIgetOrderRequest)|-|-|

### Return type

ApiResponse<[**GetOrder200Response**](GetOrder200Response.md)>


### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Default Response |  -  |
| **403** | Default Response |  -  |
| **404** | Default Response |  -  |


<a id="APIgetOrderRequest"></a>
## APIgetOrderRequest
### Properties

|     Name      |    Type       | Description   |     Notes    |
| ------------- | ------------- | ------------- | -------------|
| **orgId** | **String** | Organization ID. | |
| **orderId** | **String** | Order ID. | |



## listOrders

> ListOrders200Response listOrders(listOrdersRequest)

List orders

Returns a paginated list of orders for an organization, filterable by status, channel, search term and an advanced filter definition.

### Example

```java
// Import classes:
import com.zippendo.sdk.ApiClient;
import com.zippendo.sdk.ApiException;
import com.zippendo.sdk.Configuration;
import com.zippendo.sdk.auth.*;
import com.zippendo.sdk.models.*;
import com.zippendo.sdk.api.OrdersApi;
import com.zippendo.sdk.api.OrdersApi.*;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.zippendo.com");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        OrdersApi apiInstance = new OrdersApi(defaultClient);
        String orgId = "org_8f3kd92ld0"; // String | Organization ID
        Integer page = 1; // Integer | Page number (1-based)
        Integer limit = 20; // Integer | Items per page (max 100)
        String brandId = "brnd_8f3kd92ld0"; // String | Filter by brand. Pass a brand ID, or \"none\" for records not assigned to any brand.
        String brandScope = "own"; // String | How the brand context narrows this list: \"own\" returns only rows assigned to the current brand (requires a brand session, a brand-bound token, or the X-Zippendo-Brand header), \"shared\" returns only unassigned organization-wide rows, \"both\" (default) returns both. The X-Zippendo-Brand-Scope header supplies a default when the parameter is omitted. For strictly brand-owned records (orders, shipments), a brand-scoped request combined with \"shared\" returns no rows, since those records are never visible organization-wide from within a brand context.
        String status = "pending"; // String | Order fulfillment status derived from its shipments.
        String orderChannelId = "clz9k2f0a0001abcd1234efgh"; // String | Filter by order channel ID.
        String search = "Anna"; // String | Search by order number or customer name/email.
        String filter = "{\"conjunction\":\"and\",\"conditions\":[{\"id\":\"c_1\",\"field\":\"status\",\"operator\":\"in\",\"value\":[\"pending\",\"processing\"]}]}"; // String | Advanced filter as a JSON-encoded definition: a `conjunction` (`and`/`or`) over `conditions`, each `{ id, field, operator, value }` or a nested group. Fields and operators per list are documented under Filtering lists in the API overview. An invalid filter returns 400 `FILTER_INVALID`.
        try {
            APIlistOrdersRequest request = APIlistOrdersRequest.newBuilder()
                .orgId(orgId)
                .page(page)
                .limit(limit)
                .brandId(brandId)
                .brandScope(brandScope)
                .status(status)
                .orderChannelId(orderChannelId)
                .search(search)
                .filter(filter)
                .build();
            ListOrders200Response result = apiInstance.listOrders(request);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling OrdersApi#listOrders");
            System.err.println("Status code: " + e.getCode());
            System.err.println("Reason: " + e.getResponseBody());
            System.err.println("Response headers: " + e.getResponseHeaders());
            e.printStackTrace();
        }
    }
}
```

### Parameters

|    Name      |    Type       | Description   |     Notes    |
|------------- | ------------- | ------------- | -------------|
| listOrdersRequest | [**APIlistOrdersRequest**](OrdersApi.md#APIlistOrdersRequest)|-|-|

### Return type

[**ListOrders200Response**](ListOrders200Response.md)


### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Default Response |  -  |
| **400** | Default Response |  -  |
| **403** | Default Response |  -  |

## listOrdersWithHttpInfo

> ApiResponse<ListOrders200Response> listOrdersWithHttpInfo(listOrdersRequest)

List orders

Returns a paginated list of orders for an organization, filterable by status, channel, search term and an advanced filter definition.

### Example

```java
// Import classes:
import com.zippendo.sdk.ApiClient;
import com.zippendo.sdk.ApiException;
import com.zippendo.sdk.ApiResponse;
import com.zippendo.sdk.Configuration;
import com.zippendo.sdk.auth.*;
import com.zippendo.sdk.models.*;
import com.zippendo.sdk.api.OrdersApi;
import com.zippendo.sdk.api.OrdersApi.*;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.zippendo.com");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        OrdersApi apiInstance = new OrdersApi(defaultClient);
        String orgId = "org_8f3kd92ld0"; // String | Organization ID
        Integer page = 1; // Integer | Page number (1-based)
        Integer limit = 20; // Integer | Items per page (max 100)
        String brandId = "brnd_8f3kd92ld0"; // String | Filter by brand. Pass a brand ID, or \"none\" for records not assigned to any brand.
        String brandScope = "own"; // String | How the brand context narrows this list: \"own\" returns only rows assigned to the current brand (requires a brand session, a brand-bound token, or the X-Zippendo-Brand header), \"shared\" returns only unassigned organization-wide rows, \"both\" (default) returns both. The X-Zippendo-Brand-Scope header supplies a default when the parameter is omitted. For strictly brand-owned records (orders, shipments), a brand-scoped request combined with \"shared\" returns no rows, since those records are never visible organization-wide from within a brand context.
        String status = "pending"; // String | Order fulfillment status derived from its shipments.
        String orderChannelId = "clz9k2f0a0001abcd1234efgh"; // String | Filter by order channel ID.
        String search = "Anna"; // String | Search by order number or customer name/email.
        String filter = "{\"conjunction\":\"and\",\"conditions\":[{\"id\":\"c_1\",\"field\":\"status\",\"operator\":\"in\",\"value\":[\"pending\",\"processing\"]}]}"; // String | Advanced filter as a JSON-encoded definition: a `conjunction` (`and`/`or`) over `conditions`, each `{ id, field, operator, value }` or a nested group. Fields and operators per list are documented under Filtering lists in the API overview. An invalid filter returns 400 `FILTER_INVALID`.
        try {
            APIlistOrdersRequest request = APIlistOrdersRequest.newBuilder()
                .orgId(orgId)
                .page(page)
                .limit(limit)
                .brandId(brandId)
                .brandScope(brandScope)
                .status(status)
                .orderChannelId(orderChannelId)
                .search(search)
                .filter(filter)
                .build();
            ApiResponse<ListOrders200Response> response = apiInstance.listOrdersWithHttpInfo(request);
            System.out.println("Status code: " + response.getStatusCode());
            System.out.println("Response headers: " + response.getHeaders());
            System.out.println("Response body: " + response.getData());
        } catch (ApiException e) {
            System.err.println("Exception when calling OrdersApi#listOrders");
            System.err.println("Status code: " + e.getCode());
            System.err.println("Response headers: " + e.getResponseHeaders());
            System.err.println("Reason: " + e.getResponseBody());
            e.printStackTrace();
        }
    }
}
```

### Parameters

|    Name      |    Type       | Description   |     Notes    |
|------------- | ------------- | ------------- | -------------|
| listOrdersRequest | [**APIlistOrdersRequest**](OrdersApi.md#APIlistOrdersRequest)|-|-|

### Return type

ApiResponse<[**ListOrders200Response**](ListOrders200Response.md)>


### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Default Response |  -  |
| **400** | Default Response |  -  |
| **403** | Default Response |  -  |


<a id="APIlistOrdersRequest"></a>
## APIlistOrdersRequest
### Properties

|     Name      |    Type       | Description   |     Notes    |
| ------------- | ------------- | ------------- | -------------|
| **orgId** | **String** | Organization ID | |
| **page** | **Integer** | Page number (1-based) | [optional] [default to 1] |
| **limit** | **Integer** | Items per page (max 100) | [optional] [default to 20] |
| **brandId** | **String** | Filter by brand. Pass a brand ID, or \&quot;none\&quot; for records not assigned to any brand. | [optional] |
| **brandScope** | **String** | How the brand context narrows this list: \&quot;own\&quot; returns only rows assigned to the current brand (requires a brand session, a brand-bound token, or the X-Zippendo-Brand header), \&quot;shared\&quot; returns only unassigned organization-wide rows, \&quot;both\&quot; (default) returns both. The X-Zippendo-Brand-Scope header supplies a default when the parameter is omitted. For strictly brand-owned records (orders, shipments), a brand-scoped request combined with \&quot;shared\&quot; returns no rows, since those records are never visible organization-wide from within a brand context. | [optional] [enum: own, shared, both] |
| **status** | **String** | Order fulfillment status derived from its shipments. | [optional] [enum: pending, processing, partially_fulfilled, fulfilled, error, cancelled] |
| **orderChannelId** | **String** | Filter by order channel ID. | [optional] |
| **search** | **String** | Search by order number or customer name/email. | [optional] |
| **filter** | **String** | Advanced filter as a JSON-encoded definition: a &#x60;conjunction&#x60; (&#x60;and&#x60;/&#x60;or&#x60;) over &#x60;conditions&#x60;, each &#x60;{ id, field, operator, value }&#x60; or a nested group. Fields and operators per list are documented under Filtering lists in the API overview. An invalid filter returns 400 &#x60;FILTER_INVALID&#x60;. | [optional] |



## updateOrder

> CreateOrder201Response updateOrder(updateOrderRequest)

Update order

Updates an order that is not yet fulfilled or cancelled.

### Example

```java
// Import classes:
import com.zippendo.sdk.ApiClient;
import com.zippendo.sdk.ApiException;
import com.zippendo.sdk.Configuration;
import com.zippendo.sdk.auth.*;
import com.zippendo.sdk.models.*;
import com.zippendo.sdk.api.OrdersApi;
import com.zippendo.sdk.api.OrdersApi.*;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.zippendo.com");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        OrdersApi apiInstance = new OrdersApi(defaultClient);
        String orgId = "clz9k2f0a0000abcd0000zzzz"; // String | Organization ID.
        String orderId = "clz9k2f0a0003abcd9012mnop"; // String | Order ID.
        UpdateOrderRequest updateOrderRequest = new UpdateOrderRequest(); // UpdateOrderRequest | 
        try {
            APIupdateOrderRequest request = APIupdateOrderRequest.newBuilder()
                .orgId(orgId)
                .orderId(orderId)
                .updateOrderRequest(updateOrderRequest)
                .build();
            CreateOrder201Response result = apiInstance.updateOrder(request);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling OrdersApi#updateOrder");
            System.err.println("Status code: " + e.getCode());
            System.err.println("Reason: " + e.getResponseBody());
            System.err.println("Response headers: " + e.getResponseHeaders());
            e.printStackTrace();
        }
    }
}
```

### Parameters

|    Name      |    Type       | Description   |     Notes    |
|------------- | ------------- | ------------- | -------------|
| updateOrderRequest | [**APIupdateOrderRequest**](OrdersApi.md#APIupdateOrderRequest)|-|-|

### Return type

[**CreateOrder201Response**](CreateOrder201Response.md)


### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Default Response |  -  |
| **400** | Default Response |  -  |
| **403** | Default Response |  -  |
| **404** | Default Response |  -  |

## updateOrderWithHttpInfo

> ApiResponse<CreateOrder201Response> updateOrderWithHttpInfo(updateOrderRequest)

Update order

Updates an order that is not yet fulfilled or cancelled.

### Example

```java
// Import classes:
import com.zippendo.sdk.ApiClient;
import com.zippendo.sdk.ApiException;
import com.zippendo.sdk.ApiResponse;
import com.zippendo.sdk.Configuration;
import com.zippendo.sdk.auth.*;
import com.zippendo.sdk.models.*;
import com.zippendo.sdk.api.OrdersApi;
import com.zippendo.sdk.api.OrdersApi.*;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.zippendo.com");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        OrdersApi apiInstance = new OrdersApi(defaultClient);
        String orgId = "clz9k2f0a0000abcd0000zzzz"; // String | Organization ID.
        String orderId = "clz9k2f0a0003abcd9012mnop"; // String | Order ID.
        UpdateOrderRequest updateOrderRequest = new UpdateOrderRequest(); // UpdateOrderRequest | 
        try {
            APIupdateOrderRequest request = APIupdateOrderRequest.newBuilder()
                .orgId(orgId)
                .orderId(orderId)
                .updateOrderRequest(updateOrderRequest)
                .build();
            ApiResponse<CreateOrder201Response> response = apiInstance.updateOrderWithHttpInfo(request);
            System.out.println("Status code: " + response.getStatusCode());
            System.out.println("Response headers: " + response.getHeaders());
            System.out.println("Response body: " + response.getData());
        } catch (ApiException e) {
            System.err.println("Exception when calling OrdersApi#updateOrder");
            System.err.println("Status code: " + e.getCode());
            System.err.println("Response headers: " + e.getResponseHeaders());
            System.err.println("Reason: " + e.getResponseBody());
            e.printStackTrace();
        }
    }
}
```

### Parameters

|    Name      |    Type       | Description   |     Notes    |
|------------- | ------------- | ------------- | -------------|
| updateOrderRequest | [**APIupdateOrderRequest**](OrdersApi.md#APIupdateOrderRequest)|-|-|

### Return type

ApiResponse<[**CreateOrder201Response**](CreateOrder201Response.md)>


### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Default Response |  -  |
| **400** | Default Response |  -  |
| **403** | Default Response |  -  |
| **404** | Default Response |  -  |


<a id="APIupdateOrderRequest"></a>
## APIupdateOrderRequest
### Properties

|     Name      |    Type       | Description   |     Notes    |
| ------------- | ------------- | ------------- | -------------|
| **orgId** | **String** | Organization ID. | |
| **orderId** | **String** | Order ID. | |
| **updateOrderRequest** | [**UpdateOrderRequest**](UpdateOrderRequest.md) |  | |


