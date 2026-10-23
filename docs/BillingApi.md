# BillingApi

All URIs are relative to *https://api.zippendo.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**getBillingUsage**](BillingApi.md#getBillingUsage) | **GET** /orgs/{orgId}/billing/usage | Get usage |
| [**getBillingUsageWithHttpInfo**](BillingApi.md#getBillingUsageWithHttpInfo) | **GET** /orgs/{orgId}/billing/usage | Get usage |



## getBillingUsage

> GetBillingUsage200Response getBillingUsage(getBillingUsageRequest)

Get usage

Get detailed usage statistics for the current billing period.

### Example

```java
// Import classes:
import com.zippendo.sdk.ApiClient;
import com.zippendo.sdk.ApiException;
import com.zippendo.sdk.Configuration;
import com.zippendo.sdk.auth.*;
import com.zippendo.sdk.models.*;
import com.zippendo.sdk.api.BillingApi;
import com.zippendo.sdk.api.BillingApi.*;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.zippendo.com");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        BillingApi apiInstance = new BillingApi(defaultClient);
        String orgId = "org_8f3kd92ld0"; // String | Organization ID
        try {
            APIgetBillingUsageRequest request = APIgetBillingUsageRequest.newBuilder()
                .orgId(orgId)
                .build();
            GetBillingUsage200Response result = apiInstance.getBillingUsage(request);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling BillingApi#getBillingUsage");
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
| getBillingUsageRequest | [**APIgetBillingUsageRequest**](BillingApi.md#APIgetBillingUsageRequest)|-|-|

### Return type

[**GetBillingUsage200Response**](GetBillingUsage200Response.md)


### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Default Response |  -  |
| **401** | Default Response |  -  |
| **403** | Default Response |  -  |

## getBillingUsageWithHttpInfo

> ApiResponse<GetBillingUsage200Response> getBillingUsageWithHttpInfo(getBillingUsageRequest)

Get usage

Get detailed usage statistics for the current billing period.

### Example

```java
// Import classes:
import com.zippendo.sdk.ApiClient;
import com.zippendo.sdk.ApiException;
import com.zippendo.sdk.ApiResponse;
import com.zippendo.sdk.Configuration;
import com.zippendo.sdk.auth.*;
import com.zippendo.sdk.models.*;
import com.zippendo.sdk.api.BillingApi;
import com.zippendo.sdk.api.BillingApi.*;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.zippendo.com");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        BillingApi apiInstance = new BillingApi(defaultClient);
        String orgId = "org_8f3kd92ld0"; // String | Organization ID
        try {
            APIgetBillingUsageRequest request = APIgetBillingUsageRequest.newBuilder()
                .orgId(orgId)
                .build();
            ApiResponse<GetBillingUsage200Response> response = apiInstance.getBillingUsageWithHttpInfo(request);
            System.out.println("Status code: " + response.getStatusCode());
            System.out.println("Response headers: " + response.getHeaders());
            System.out.println("Response body: " + response.getData());
        } catch (ApiException e) {
            System.err.println("Exception when calling BillingApi#getBillingUsage");
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
| getBillingUsageRequest | [**APIgetBillingUsageRequest**](BillingApi.md#APIgetBillingUsageRequest)|-|-|

### Return type

ApiResponse<[**GetBillingUsage200Response**](GetBillingUsage200Response.md)>


### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Default Response |  -  |
| **401** | Default Response |  -  |
| **403** | Default Response |  -  |


<a id="APIgetBillingUsageRequest"></a>
## APIgetBillingUsageRequest
### Properties

|     Name      |    Type       | Description   |     Notes    |
| ------------- | ------------- | ------------- | -------------|
| **orgId** | **String** | Organization ID | |


