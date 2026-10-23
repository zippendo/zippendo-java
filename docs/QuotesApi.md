# QuotesApi

All URIs are relative to *https://api.zippendo.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**createShippingQuote**](QuotesApi.md#createShippingQuote) | **POST** /orgs/{orgId}/shipping-quote | Calculate shipping rates |
| [**createShippingQuoteWithHttpInfo**](QuotesApi.md#createShippingQuoteWithHttpInfo) | **POST** /orgs/{orgId}/shipping-quote | Calculate shipping rates |



## createShippingQuote

> CreateShippingQuote200Response createShippingQuote(createShippingQuoteRequest)

Calculate shipping rates

Calculates shipping rates from configured shipping rules based on cart items and destination.

### Example

```java
// Import classes:
import com.zippendo.sdk.ApiClient;
import com.zippendo.sdk.ApiException;
import com.zippendo.sdk.Configuration;
import com.zippendo.sdk.auth.*;
import com.zippendo.sdk.models.*;
import com.zippendo.sdk.api.QuotesApi;
import com.zippendo.sdk.api.QuotesApi.*;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.zippendo.com");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        QuotesApi apiInstance = new QuotesApi(defaultClient);
        String orgId = "org_01HZX9K2QF"; // String | Organization ID
        CreateShippingQuoteRequest createShippingQuoteRequest = new CreateShippingQuoteRequest(); // CreateShippingQuoteRequest | 
        try {
            APIcreateShippingQuoteRequest request = APIcreateShippingQuoteRequest.newBuilder()
                .orgId(orgId)
                .createShippingQuoteRequest(createShippingQuoteRequest)
                .build();
            CreateShippingQuote200Response result = apiInstance.createShippingQuote(request);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling QuotesApi#createShippingQuote");
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
| createShippingQuoteRequest | [**APIcreateShippingQuoteRequest**](QuotesApi.md#APIcreateShippingQuoteRequest)|-|-|

### Return type

[**CreateShippingQuote200Response**](CreateShippingQuote200Response.md)


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
| **404** | Default Response |  -  |

## createShippingQuoteWithHttpInfo

> ApiResponse<CreateShippingQuote200Response> createShippingQuoteWithHttpInfo(createShippingQuoteRequest)

Calculate shipping rates

Calculates shipping rates from configured shipping rules based on cart items and destination.

### Example

```java
// Import classes:
import com.zippendo.sdk.ApiClient;
import com.zippendo.sdk.ApiException;
import com.zippendo.sdk.ApiResponse;
import com.zippendo.sdk.Configuration;
import com.zippendo.sdk.auth.*;
import com.zippendo.sdk.models.*;
import com.zippendo.sdk.api.QuotesApi;
import com.zippendo.sdk.api.QuotesApi.*;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.zippendo.com");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        QuotesApi apiInstance = new QuotesApi(defaultClient);
        String orgId = "org_01HZX9K2QF"; // String | Organization ID
        CreateShippingQuoteRequest createShippingQuoteRequest = new CreateShippingQuoteRequest(); // CreateShippingQuoteRequest | 
        try {
            APIcreateShippingQuoteRequest request = APIcreateShippingQuoteRequest.newBuilder()
                .orgId(orgId)
                .createShippingQuoteRequest(createShippingQuoteRequest)
                .build();
            ApiResponse<CreateShippingQuote200Response> response = apiInstance.createShippingQuoteWithHttpInfo(request);
            System.out.println("Status code: " + response.getStatusCode());
            System.out.println("Response headers: " + response.getHeaders());
            System.out.println("Response body: " + response.getData());
        } catch (ApiException e) {
            System.err.println("Exception when calling QuotesApi#createShippingQuote");
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
| createShippingQuoteRequest | [**APIcreateShippingQuoteRequest**](QuotesApi.md#APIcreateShippingQuoteRequest)|-|-|

### Return type

ApiResponse<[**CreateShippingQuote200Response**](CreateShippingQuote200Response.md)>


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
| **404** | Default Response |  -  |


<a id="APIcreateShippingQuoteRequest"></a>
## APIcreateShippingQuoteRequest
### Properties

|     Name      |    Type       | Description   |     Notes    |
| ------------- | ------------- | ------------- | -------------|
| **orgId** | **String** | Organization ID | |
| **createShippingQuoteRequest** | [**CreateShippingQuoteRequest**](CreateShippingQuoteRequest.md) |  | |


