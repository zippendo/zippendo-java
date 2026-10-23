# RulesApi

All URIs are relative to *https://api.zippendo.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**createShippingRule**](RulesApi.md#createShippingRule) | **POST** /orgs/{orgId}/shipping-rules | Create shipping rule |
| [**createShippingRuleWithHttpInfo**](RulesApi.md#createShippingRuleWithHttpInfo) | **POST** /orgs/{orgId}/shipping-rules | Create shipping rule |
| [**deleteShippingRule**](RulesApi.md#deleteShippingRule) | **DELETE** /orgs/{orgId}/shipping-rules/{ruleId} | Delete shipping rule |
| [**deleteShippingRuleWithHttpInfo**](RulesApi.md#deleteShippingRuleWithHttpInfo) | **DELETE** /orgs/{orgId}/shipping-rules/{ruleId} | Delete shipping rule |
| [**getShippingRule**](RulesApi.md#getShippingRule) | **GET** /orgs/{orgId}/shipping-rules/{ruleId} | Get shipping rule |
| [**getShippingRuleWithHttpInfo**](RulesApi.md#getShippingRuleWithHttpInfo) | **GET** /orgs/{orgId}/shipping-rules/{ruleId} | Get shipping rule |
| [**listShippingRules**](RulesApi.md#listShippingRules) | **GET** /orgs/{orgId}/shipping-rules | List shipping rules |
| [**listShippingRulesWithHttpInfo**](RulesApi.md#listShippingRulesWithHttpInfo) | **GET** /orgs/{orgId}/shipping-rules | List shipping rules |
| [**updateShippingRule**](RulesApi.md#updateShippingRule) | **PATCH** /orgs/{orgId}/shipping-rules/{ruleId} | Update shipping rule |
| [**updateShippingRuleWithHttpInfo**](RulesApi.md#updateShippingRuleWithHttpInfo) | **PATCH** /orgs/{orgId}/shipping-rules/{ruleId} | Update shipping rule |



## createShippingRule

> CreateShippingRule201Response createShippingRule(createShippingRuleRequest)

Create shipping rule

Creates a new shipping rule with conditions and carrier product for the organization.

### Example

```java
// Import classes:
import com.zippendo.sdk.ApiClient;
import com.zippendo.sdk.ApiException;
import com.zippendo.sdk.Configuration;
import com.zippendo.sdk.auth.*;
import com.zippendo.sdk.models.*;
import com.zippendo.sdk.api.RulesApi;
import com.zippendo.sdk.api.RulesApi.*;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.zippendo.com");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        RulesApi apiInstance = new RulesApi(defaultClient);
        String orgId = "org_01HZX9K2QF"; // String | Organization ID
        CreateShippingRuleRequest createShippingRuleRequest = new CreateShippingRuleRequest(); // CreateShippingRuleRequest | 
        try {
            APIcreateShippingRuleRequest request = APIcreateShippingRuleRequest.newBuilder()
                .orgId(orgId)
                .createShippingRuleRequest(createShippingRuleRequest)
                .build();
            CreateShippingRule201Response result = apiInstance.createShippingRule(request);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling RulesApi#createShippingRule");
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
| createShippingRuleRequest | [**APIcreateShippingRuleRequest**](RulesApi.md#APIcreateShippingRuleRequest)|-|-|

### Return type

[**CreateShippingRule201Response**](CreateShippingRule201Response.md)


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

## createShippingRuleWithHttpInfo

> ApiResponse<CreateShippingRule201Response> createShippingRuleWithHttpInfo(createShippingRuleRequest)

Create shipping rule

Creates a new shipping rule with conditions and carrier product for the organization.

### Example

```java
// Import classes:
import com.zippendo.sdk.ApiClient;
import com.zippendo.sdk.ApiException;
import com.zippendo.sdk.ApiResponse;
import com.zippendo.sdk.Configuration;
import com.zippendo.sdk.auth.*;
import com.zippendo.sdk.models.*;
import com.zippendo.sdk.api.RulesApi;
import com.zippendo.sdk.api.RulesApi.*;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.zippendo.com");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        RulesApi apiInstance = new RulesApi(defaultClient);
        String orgId = "org_01HZX9K2QF"; // String | Organization ID
        CreateShippingRuleRequest createShippingRuleRequest = new CreateShippingRuleRequest(); // CreateShippingRuleRequest | 
        try {
            APIcreateShippingRuleRequest request = APIcreateShippingRuleRequest.newBuilder()
                .orgId(orgId)
                .createShippingRuleRequest(createShippingRuleRequest)
                .build();
            ApiResponse<CreateShippingRule201Response> response = apiInstance.createShippingRuleWithHttpInfo(request);
            System.out.println("Status code: " + response.getStatusCode());
            System.out.println("Response headers: " + response.getHeaders());
            System.out.println("Response body: " + response.getData());
        } catch (ApiException e) {
            System.err.println("Exception when calling RulesApi#createShippingRule");
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
| createShippingRuleRequest | [**APIcreateShippingRuleRequest**](RulesApi.md#APIcreateShippingRuleRequest)|-|-|

### Return type

ApiResponse<[**CreateShippingRule201Response**](CreateShippingRule201Response.md)>


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


<a id="APIcreateShippingRuleRequest"></a>
## APIcreateShippingRuleRequest
### Properties

|     Name      |    Type       | Description   |     Notes    |
| ------------- | ------------- | ------------- | -------------|
| **orgId** | **String** | Organization ID | |
| **createShippingRuleRequest** | [**CreateShippingRuleRequest**](CreateShippingRuleRequest.md) |  | |



## deleteShippingRule

> DeleteShippingRule200Response deleteShippingRule(deleteShippingRuleRequest)

Delete shipping rule

Deletes a shipping rule belonging to the organization.

### Example

```java
// Import classes:
import com.zippendo.sdk.ApiClient;
import com.zippendo.sdk.ApiException;
import com.zippendo.sdk.Configuration;
import com.zippendo.sdk.auth.*;
import com.zippendo.sdk.models.*;
import com.zippendo.sdk.api.RulesApi;
import com.zippendo.sdk.api.RulesApi.*;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.zippendo.com");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        RulesApi apiInstance = new RulesApi(defaultClient);
        String orgId = "org_01HZX9K2QF"; // String | Organization ID
        String ruleId = "rule_01HZX9K2QF"; // String | Shipping Rule ID
        try {
            APIdeleteShippingRuleRequest request = APIdeleteShippingRuleRequest.newBuilder()
                .orgId(orgId)
                .ruleId(ruleId)
                .build();
            DeleteShippingRule200Response result = apiInstance.deleteShippingRule(request);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling RulesApi#deleteShippingRule");
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
| deleteShippingRuleRequest | [**APIdeleteShippingRuleRequest**](RulesApi.md#APIdeleteShippingRuleRequest)|-|-|

### Return type

[**DeleteShippingRule200Response**](DeleteShippingRule200Response.md)


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

## deleteShippingRuleWithHttpInfo

> ApiResponse<DeleteShippingRule200Response> deleteShippingRuleWithHttpInfo(deleteShippingRuleRequest)

Delete shipping rule

Deletes a shipping rule belonging to the organization.

### Example

```java
// Import classes:
import com.zippendo.sdk.ApiClient;
import com.zippendo.sdk.ApiException;
import com.zippendo.sdk.ApiResponse;
import com.zippendo.sdk.Configuration;
import com.zippendo.sdk.auth.*;
import com.zippendo.sdk.models.*;
import com.zippendo.sdk.api.RulesApi;
import com.zippendo.sdk.api.RulesApi.*;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.zippendo.com");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        RulesApi apiInstance = new RulesApi(defaultClient);
        String orgId = "org_01HZX9K2QF"; // String | Organization ID
        String ruleId = "rule_01HZX9K2QF"; // String | Shipping Rule ID
        try {
            APIdeleteShippingRuleRequest request = APIdeleteShippingRuleRequest.newBuilder()
                .orgId(orgId)
                .ruleId(ruleId)
                .build();
            ApiResponse<DeleteShippingRule200Response> response = apiInstance.deleteShippingRuleWithHttpInfo(request);
            System.out.println("Status code: " + response.getStatusCode());
            System.out.println("Response headers: " + response.getHeaders());
            System.out.println("Response body: " + response.getData());
        } catch (ApiException e) {
            System.err.println("Exception when calling RulesApi#deleteShippingRule");
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
| deleteShippingRuleRequest | [**APIdeleteShippingRuleRequest**](RulesApi.md#APIdeleteShippingRuleRequest)|-|-|

### Return type

ApiResponse<[**DeleteShippingRule200Response**](DeleteShippingRule200Response.md)>


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


<a id="APIdeleteShippingRuleRequest"></a>
## APIdeleteShippingRuleRequest
### Properties

|     Name      |    Type       | Description   |     Notes    |
| ------------- | ------------- | ------------- | -------------|
| **orgId** | **String** | Organization ID | |
| **ruleId** | **String** | Shipping Rule ID | |



## getShippingRule

> ListShippingRules200ResponseDataInner getShippingRule(getShippingRuleRequest)

Get shipping rule

Returns a single shipping rule with its carrier, address and printer relations.

### Example

```java
// Import classes:
import com.zippendo.sdk.ApiClient;
import com.zippendo.sdk.ApiException;
import com.zippendo.sdk.Configuration;
import com.zippendo.sdk.auth.*;
import com.zippendo.sdk.models.*;
import com.zippendo.sdk.api.RulesApi;
import com.zippendo.sdk.api.RulesApi.*;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.zippendo.com");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        RulesApi apiInstance = new RulesApi(defaultClient);
        String orgId = "org_01HZX9K2QF"; // String | Organization ID
        String ruleId = "rule_01HZX9K2QF"; // String | Shipping Rule ID
        try {
            APIgetShippingRuleRequest request = APIgetShippingRuleRequest.newBuilder()
                .orgId(orgId)
                .ruleId(ruleId)
                .build();
            ListShippingRules200ResponseDataInner result = apiInstance.getShippingRule(request);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling RulesApi#getShippingRule");
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
| getShippingRuleRequest | [**APIgetShippingRuleRequest**](RulesApi.md#APIgetShippingRuleRequest)|-|-|

### Return type

[**ListShippingRules200ResponseDataInner**](ListShippingRules200ResponseDataInner.md)


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

## getShippingRuleWithHttpInfo

> ApiResponse<ListShippingRules200ResponseDataInner> getShippingRuleWithHttpInfo(getShippingRuleRequest)

Get shipping rule

Returns a single shipping rule with its carrier, address and printer relations.

### Example

```java
// Import classes:
import com.zippendo.sdk.ApiClient;
import com.zippendo.sdk.ApiException;
import com.zippendo.sdk.ApiResponse;
import com.zippendo.sdk.Configuration;
import com.zippendo.sdk.auth.*;
import com.zippendo.sdk.models.*;
import com.zippendo.sdk.api.RulesApi;
import com.zippendo.sdk.api.RulesApi.*;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.zippendo.com");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        RulesApi apiInstance = new RulesApi(defaultClient);
        String orgId = "org_01HZX9K2QF"; // String | Organization ID
        String ruleId = "rule_01HZX9K2QF"; // String | Shipping Rule ID
        try {
            APIgetShippingRuleRequest request = APIgetShippingRuleRequest.newBuilder()
                .orgId(orgId)
                .ruleId(ruleId)
                .build();
            ApiResponse<ListShippingRules200ResponseDataInner> response = apiInstance.getShippingRuleWithHttpInfo(request);
            System.out.println("Status code: " + response.getStatusCode());
            System.out.println("Response headers: " + response.getHeaders());
            System.out.println("Response body: " + response.getData());
        } catch (ApiException e) {
            System.err.println("Exception when calling RulesApi#getShippingRule");
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
| getShippingRuleRequest | [**APIgetShippingRuleRequest**](RulesApi.md#APIgetShippingRuleRequest)|-|-|

### Return type

ApiResponse<[**ListShippingRules200ResponseDataInner**](ListShippingRules200ResponseDataInner.md)>


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


<a id="APIgetShippingRuleRequest"></a>
## APIgetShippingRuleRequest
### Properties

|     Name      |    Type       | Description   |     Notes    |
| ------------- | ------------- | ------------- | -------------|
| **orgId** | **String** | Organization ID | |
| **ruleId** | **String** | Shipping Rule ID | |



## listShippingRules

> ListShippingRules200Response listShippingRules(listShippingRulesRequest)

List shipping rules

Returns a paginated list of shipping rules for the organization with their relations.

### Example

```java
// Import classes:
import com.zippendo.sdk.ApiClient;
import com.zippendo.sdk.ApiException;
import com.zippendo.sdk.Configuration;
import com.zippendo.sdk.auth.*;
import com.zippendo.sdk.models.*;
import com.zippendo.sdk.api.RulesApi;
import com.zippendo.sdk.api.RulesApi.*;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.zippendo.com");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        RulesApi apiInstance = new RulesApi(defaultClient);
        String orgId = "org_01HZX9K2QF"; // String | Organization ID
        Integer page = 1; // Integer | Page number (1-based)
        Integer limit = 20; // Integer | Items per page (max 100)
        String brandId = "brnd_8f3kd92ld0"; // String | Filter by brand. Pass a brand ID, or \"none\" for records not assigned to any brand.
        String brandScope = "own"; // String | How the brand context narrows this list: \"own\" returns only rows assigned to the current brand (requires a brand session, a brand-bound token, or the X-Zippendo-Brand header), \"shared\" returns only unassigned organization-wide rows, \"both\" (default) returns both. The X-Zippendo-Brand-Scope header supplies a default when the parameter is omitted. For strictly brand-owned records (orders, shipments), a brand-scoped request combined with \"shared\" returns no rows, since those records are never visible organization-wide from within a brand context.
        String carrierId = "carr_01HZX9K2QF"; // String | Filter by carrier.
        String search = "Home delivery"; // String | Search by rule name.
        try {
            APIlistShippingRulesRequest request = APIlistShippingRulesRequest.newBuilder()
                .orgId(orgId)
                .page(page)
                .limit(limit)
                .brandId(brandId)
                .brandScope(brandScope)
                .carrierId(carrierId)
                .search(search)
                .build();
            ListShippingRules200Response result = apiInstance.listShippingRules(request);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling RulesApi#listShippingRules");
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
| listShippingRulesRequest | [**APIlistShippingRulesRequest**](RulesApi.md#APIlistShippingRulesRequest)|-|-|

### Return type

[**ListShippingRules200Response**](ListShippingRules200Response.md)


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

## listShippingRulesWithHttpInfo

> ApiResponse<ListShippingRules200Response> listShippingRulesWithHttpInfo(listShippingRulesRequest)

List shipping rules

Returns a paginated list of shipping rules for the organization with their relations.

### Example

```java
// Import classes:
import com.zippendo.sdk.ApiClient;
import com.zippendo.sdk.ApiException;
import com.zippendo.sdk.ApiResponse;
import com.zippendo.sdk.Configuration;
import com.zippendo.sdk.auth.*;
import com.zippendo.sdk.models.*;
import com.zippendo.sdk.api.RulesApi;
import com.zippendo.sdk.api.RulesApi.*;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.zippendo.com");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        RulesApi apiInstance = new RulesApi(defaultClient);
        String orgId = "org_01HZX9K2QF"; // String | Organization ID
        Integer page = 1; // Integer | Page number (1-based)
        Integer limit = 20; // Integer | Items per page (max 100)
        String brandId = "brnd_8f3kd92ld0"; // String | Filter by brand. Pass a brand ID, or \"none\" for records not assigned to any brand.
        String brandScope = "own"; // String | How the brand context narrows this list: \"own\" returns only rows assigned to the current brand (requires a brand session, a brand-bound token, or the X-Zippendo-Brand header), \"shared\" returns only unassigned organization-wide rows, \"both\" (default) returns both. The X-Zippendo-Brand-Scope header supplies a default when the parameter is omitted. For strictly brand-owned records (orders, shipments), a brand-scoped request combined with \"shared\" returns no rows, since those records are never visible organization-wide from within a brand context.
        String carrierId = "carr_01HZX9K2QF"; // String | Filter by carrier.
        String search = "Home delivery"; // String | Search by rule name.
        try {
            APIlistShippingRulesRequest request = APIlistShippingRulesRequest.newBuilder()
                .orgId(orgId)
                .page(page)
                .limit(limit)
                .brandId(brandId)
                .brandScope(brandScope)
                .carrierId(carrierId)
                .search(search)
                .build();
            ApiResponse<ListShippingRules200Response> response = apiInstance.listShippingRulesWithHttpInfo(request);
            System.out.println("Status code: " + response.getStatusCode());
            System.out.println("Response headers: " + response.getHeaders());
            System.out.println("Response body: " + response.getData());
        } catch (ApiException e) {
            System.err.println("Exception when calling RulesApi#listShippingRules");
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
| listShippingRulesRequest | [**APIlistShippingRulesRequest**](RulesApi.md#APIlistShippingRulesRequest)|-|-|

### Return type

ApiResponse<[**ListShippingRules200Response**](ListShippingRules200Response.md)>


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


<a id="APIlistShippingRulesRequest"></a>
## APIlistShippingRulesRequest
### Properties

|     Name      |    Type       | Description   |     Notes    |
| ------------- | ------------- | ------------- | -------------|
| **orgId** | **String** | Organization ID | |
| **page** | **Integer** | Page number (1-based) | [optional] [default to 1] |
| **limit** | **Integer** | Items per page (max 100) | [optional] [default to 20] |
| **brandId** | **String** | Filter by brand. Pass a brand ID, or \&quot;none\&quot; for records not assigned to any brand. | [optional] |
| **brandScope** | **String** | How the brand context narrows this list: \&quot;own\&quot; returns only rows assigned to the current brand (requires a brand session, a brand-bound token, or the X-Zippendo-Brand header), \&quot;shared\&quot; returns only unassigned organization-wide rows, \&quot;both\&quot; (default) returns both. The X-Zippendo-Brand-Scope header supplies a default when the parameter is omitted. For strictly brand-owned records (orders, shipments), a brand-scoped request combined with \&quot;shared\&quot; returns no rows, since those records are never visible organization-wide from within a brand context. | [optional] [enum: own, shared, both] |
| **carrierId** | **String** | Filter by carrier. | [optional] |
| **search** | **String** | Search by rule name. | [optional] |



## updateShippingRule

> CreateShippingRule201Response updateShippingRule(updateShippingRuleRequest)

Update shipping rule

Updates an existing shipping rule for the organization.

### Example

```java
// Import classes:
import com.zippendo.sdk.ApiClient;
import com.zippendo.sdk.ApiException;
import com.zippendo.sdk.Configuration;
import com.zippendo.sdk.auth.*;
import com.zippendo.sdk.models.*;
import com.zippendo.sdk.api.RulesApi;
import com.zippendo.sdk.api.RulesApi.*;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.zippendo.com");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        RulesApi apiInstance = new RulesApi(defaultClient);
        String orgId = "org_01HZX9K2QF"; // String | Organization ID
        String ruleId = "rule_01HZX9K2QF"; // String | Shipping Rule ID
        UpdateShippingRuleRequest updateShippingRuleRequest = new UpdateShippingRuleRequest(); // UpdateShippingRuleRequest | 
        try {
            APIupdateShippingRuleRequest request = APIupdateShippingRuleRequest.newBuilder()
                .orgId(orgId)
                .ruleId(ruleId)
                .updateShippingRuleRequest(updateShippingRuleRequest)
                .build();
            CreateShippingRule201Response result = apiInstance.updateShippingRule(request);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling RulesApi#updateShippingRule");
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
| updateShippingRuleRequest | [**APIupdateShippingRuleRequest**](RulesApi.md#APIupdateShippingRuleRequest)|-|-|

### Return type

[**CreateShippingRule201Response**](CreateShippingRule201Response.md)


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

## updateShippingRuleWithHttpInfo

> ApiResponse<CreateShippingRule201Response> updateShippingRuleWithHttpInfo(updateShippingRuleRequest)

Update shipping rule

Updates an existing shipping rule for the organization.

### Example

```java
// Import classes:
import com.zippendo.sdk.ApiClient;
import com.zippendo.sdk.ApiException;
import com.zippendo.sdk.ApiResponse;
import com.zippendo.sdk.Configuration;
import com.zippendo.sdk.auth.*;
import com.zippendo.sdk.models.*;
import com.zippendo.sdk.api.RulesApi;
import com.zippendo.sdk.api.RulesApi.*;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.zippendo.com");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        RulesApi apiInstance = new RulesApi(defaultClient);
        String orgId = "org_01HZX9K2QF"; // String | Organization ID
        String ruleId = "rule_01HZX9K2QF"; // String | Shipping Rule ID
        UpdateShippingRuleRequest updateShippingRuleRequest = new UpdateShippingRuleRequest(); // UpdateShippingRuleRequest | 
        try {
            APIupdateShippingRuleRequest request = APIupdateShippingRuleRequest.newBuilder()
                .orgId(orgId)
                .ruleId(ruleId)
                .updateShippingRuleRequest(updateShippingRuleRequest)
                .build();
            ApiResponse<CreateShippingRule201Response> response = apiInstance.updateShippingRuleWithHttpInfo(request);
            System.out.println("Status code: " + response.getStatusCode());
            System.out.println("Response headers: " + response.getHeaders());
            System.out.println("Response body: " + response.getData());
        } catch (ApiException e) {
            System.err.println("Exception when calling RulesApi#updateShippingRule");
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
| updateShippingRuleRequest | [**APIupdateShippingRuleRequest**](RulesApi.md#APIupdateShippingRuleRequest)|-|-|

### Return type

ApiResponse<[**CreateShippingRule201Response**](CreateShippingRule201Response.md)>


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


<a id="APIupdateShippingRuleRequest"></a>
## APIupdateShippingRuleRequest
### Properties

|     Name      |    Type       | Description   |     Notes    |
| ------------- | ------------- | ------------- | -------------|
| **orgId** | **String** | Organization ID | |
| **ruleId** | **String** | Shipping Rule ID | |
| **updateShippingRuleRequest** | [**UpdateShippingRuleRequest**](UpdateShippingRuleRequest.md) |  | |


