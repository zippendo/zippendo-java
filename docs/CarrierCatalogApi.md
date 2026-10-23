# CarrierCatalogApi

All URIs are relative to *https://api.zippendo.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**listAvailableCarriers**](CarrierCatalogApi.md#listAvailableCarriers) | **GET** /orgs/{orgId}/available-carriers | List available carriers |
| [**listAvailableCarriersWithHttpInfo**](CarrierCatalogApi.md#listAvailableCarriersWithHttpInfo) | **GET** /orgs/{orgId}/available-carriers | List available carriers |



## listAvailableCarriers

> List<ListAvailableCarriers200ResponseInner> listAvailableCarriers(listAvailableCarriersRequest)

List available carriers

Returns the carriers available to connect, as supported by the carrier server.

### Example

```java
// Import classes:
import com.zippendo.sdk.ApiClient;
import com.zippendo.sdk.ApiException;
import com.zippendo.sdk.Configuration;
import com.zippendo.sdk.auth.*;
import com.zippendo.sdk.models.*;
import com.zippendo.sdk.api.CarrierCatalogApi;
import com.zippendo.sdk.api.CarrierCatalogApi.*;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.zippendo.com");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        CarrierCatalogApi apiInstance = new CarrierCatalogApi(defaultClient);
        String orgId = "org_01HZX9K2QF"; // String | Organization ID
        try {
            APIlistAvailableCarriersRequest request = APIlistAvailableCarriersRequest.newBuilder()
                .orgId(orgId)
                .build();
            List<ListAvailableCarriers200ResponseInner> result = apiInstance.listAvailableCarriers(request);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling CarrierCatalogApi#listAvailableCarriers");
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
| listAvailableCarriersRequest | [**APIlistAvailableCarriersRequest**](CarrierCatalogApi.md#APIlistAvailableCarriersRequest)|-|-|

### Return type

[**List&lt;ListAvailableCarriers200ResponseInner&gt;**](ListAvailableCarriers200ResponseInner.md)


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
| **500** | Default Response |  -  |

## listAvailableCarriersWithHttpInfo

> ApiResponse<List<ListAvailableCarriers200ResponseInner>> listAvailableCarriersWithHttpInfo(listAvailableCarriersRequest)

List available carriers

Returns the carriers available to connect, as supported by the carrier server.

### Example

```java
// Import classes:
import com.zippendo.sdk.ApiClient;
import com.zippendo.sdk.ApiException;
import com.zippendo.sdk.ApiResponse;
import com.zippendo.sdk.Configuration;
import com.zippendo.sdk.auth.*;
import com.zippendo.sdk.models.*;
import com.zippendo.sdk.api.CarrierCatalogApi;
import com.zippendo.sdk.api.CarrierCatalogApi.*;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.zippendo.com");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        CarrierCatalogApi apiInstance = new CarrierCatalogApi(defaultClient);
        String orgId = "org_01HZX9K2QF"; // String | Organization ID
        try {
            APIlistAvailableCarriersRequest request = APIlistAvailableCarriersRequest.newBuilder()
                .orgId(orgId)
                .build();
            ApiResponse<List<ListAvailableCarriers200ResponseInner>> response = apiInstance.listAvailableCarriersWithHttpInfo(request);
            System.out.println("Status code: " + response.getStatusCode());
            System.out.println("Response headers: " + response.getHeaders());
            System.out.println("Response body: " + response.getData());
        } catch (ApiException e) {
            System.err.println("Exception when calling CarrierCatalogApi#listAvailableCarriers");
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
| listAvailableCarriersRequest | [**APIlistAvailableCarriersRequest**](CarrierCatalogApi.md#APIlistAvailableCarriersRequest)|-|-|

### Return type

ApiResponse<[**List&lt;ListAvailableCarriers200ResponseInner&gt;**](ListAvailableCarriers200ResponseInner.md)>


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
| **500** | Default Response |  -  |


<a id="APIlistAvailableCarriersRequest"></a>
## APIlistAvailableCarriersRequest
### Properties

|     Name      |    Type       | Description   |     Notes    |
| ------------- | ------------- | ------------- | -------------|
| **orgId** | **String** | Organization ID | |


