# CarriersApi

All URIs are relative to *https://api.zippendo.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**connectCarrier**](CarriersApi.md#connectCarrier) | **POST** /orgs/{orgId}/carriers | Connect carrier |
| [**connectCarrierWithHttpInfo**](CarriersApi.md#connectCarrierWithHttpInfo) | **POST** /orgs/{orgId}/carriers | Connect carrier |
| [**disconnectCarrier**](CarriersApi.md#disconnectCarrier) | **DELETE** /orgs/{orgId}/carriers/{carrierId} | Disconnect carrier |
| [**disconnectCarrierWithHttpInfo**](CarriersApi.md#disconnectCarrierWithHttpInfo) | **DELETE** /orgs/{orgId}/carriers/{carrierId} | Disconnect carrier |
| [**getCarrier**](CarriersApi.md#getCarrier) | **GET** /orgs/{orgId}/carriers/{carrierId} | Get carrier |
| [**getCarrierWithHttpInfo**](CarriersApi.md#getCarrierWithHttpInfo) | **GET** /orgs/{orgId}/carriers/{carrierId} | Get carrier |
| [**listCarrierProductServicePoints**](CarriersApi.md#listCarrierProductServicePoints) | **POST** /orgs/{orgId}/carriers/{carrierId}/products/{productId}/service-points | List product service points |
| [**listCarrierProductServicePointsWithHttpInfo**](CarriersApi.md#listCarrierProductServicePointsWithHttpInfo) | **POST** /orgs/{orgId}/carriers/{carrierId}/products/{productId}/service-points | List product service points |
| [**listCarrierProducts**](CarriersApi.md#listCarrierProducts) | **GET** /orgs/{orgId}/carriers/{carrierId}/products | List carrier products |
| [**listCarrierProductsWithHttpInfo**](CarriersApi.md#listCarrierProductsWithHttpInfo) | **GET** /orgs/{orgId}/carriers/{carrierId}/products | List carrier products |
| [**listCarriers**](CarriersApi.md#listCarriers) | **GET** /orgs/{orgId}/carriers | List carriers |
| [**listCarriersWithHttpInfo**](CarriersApi.md#listCarriersWithHttpInfo) | **GET** /orgs/{orgId}/carriers | List carriers |
| [**updateCarrier**](CarriersApi.md#updateCarrier) | **PUT** /orgs/{orgId}/carriers/{carrierId} | Update carrier |
| [**updateCarrierWithHttpInfo**](CarriersApi.md#updateCarrierWithHttpInfo) | **PUT** /orgs/{orgId}/carriers/{carrierId} | Update carrier |



## connectCarrier

> ListCarriers200ResponseDataInner connectCarrier(connectCarrierRequest)

Connect carrier

Connects a new carrier to the organization with its configuration.

### Example

```java
// Import classes:
import com.zippendo.sdk.ApiClient;
import com.zippendo.sdk.ApiException;
import com.zippendo.sdk.Configuration;
import com.zippendo.sdk.auth.*;
import com.zippendo.sdk.models.*;
import com.zippendo.sdk.api.CarriersApi;
import com.zippendo.sdk.api.CarriersApi.*;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.zippendo.com");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        CarriersApi apiInstance = new CarriersApi(defaultClient);
        String orgId = "org_01HZX9K2QF"; // String | Organization ID
        ConnectCarrierRequest connectCarrierRequest = new ConnectCarrierRequest(); // ConnectCarrierRequest | 
        try {
            APIconnectCarrierRequest request = APIconnectCarrierRequest.newBuilder()
                .orgId(orgId)
                .connectCarrierRequest(connectCarrierRequest)
                .build();
            ListCarriers200ResponseDataInner result = apiInstance.connectCarrier(request);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling CarriersApi#connectCarrier");
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
| connectCarrierRequest | [**APIconnectCarrierRequest**](CarriersApi.md#APIconnectCarrierRequest)|-|-|

### Return type

[**ListCarriers200ResponseDataInner**](ListCarriers200ResponseDataInner.md)


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

## connectCarrierWithHttpInfo

> ApiResponse<ListCarriers200ResponseDataInner> connectCarrierWithHttpInfo(connectCarrierRequest)

Connect carrier

Connects a new carrier to the organization with its configuration.

### Example

```java
// Import classes:
import com.zippendo.sdk.ApiClient;
import com.zippendo.sdk.ApiException;
import com.zippendo.sdk.ApiResponse;
import com.zippendo.sdk.Configuration;
import com.zippendo.sdk.auth.*;
import com.zippendo.sdk.models.*;
import com.zippendo.sdk.api.CarriersApi;
import com.zippendo.sdk.api.CarriersApi.*;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.zippendo.com");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        CarriersApi apiInstance = new CarriersApi(defaultClient);
        String orgId = "org_01HZX9K2QF"; // String | Organization ID
        ConnectCarrierRequest connectCarrierRequest = new ConnectCarrierRequest(); // ConnectCarrierRequest | 
        try {
            APIconnectCarrierRequest request = APIconnectCarrierRequest.newBuilder()
                .orgId(orgId)
                .connectCarrierRequest(connectCarrierRequest)
                .build();
            ApiResponse<ListCarriers200ResponseDataInner> response = apiInstance.connectCarrierWithHttpInfo(request);
            System.out.println("Status code: " + response.getStatusCode());
            System.out.println("Response headers: " + response.getHeaders());
            System.out.println("Response body: " + response.getData());
        } catch (ApiException e) {
            System.err.println("Exception when calling CarriersApi#connectCarrier");
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
| connectCarrierRequest | [**APIconnectCarrierRequest**](CarriersApi.md#APIconnectCarrierRequest)|-|-|

### Return type

ApiResponse<[**ListCarriers200ResponseDataInner**](ListCarriers200ResponseDataInner.md)>


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


<a id="APIconnectCarrierRequest"></a>
## APIconnectCarrierRequest
### Properties

|     Name      |    Type       | Description   |     Notes    |
| ------------- | ------------- | ------------- | -------------|
| **orgId** | **String** | Organization ID | |
| **connectCarrierRequest** | [**ConnectCarrierRequest**](ConnectCarrierRequest.md) |  | |



## disconnectCarrier

> String disconnectCarrier(disconnectCarrierRequest)

Disconnect carrier

Disconnects a carrier from the organization.

### Example

```java
// Import classes:
import com.zippendo.sdk.ApiClient;
import com.zippendo.sdk.ApiException;
import com.zippendo.sdk.Configuration;
import com.zippendo.sdk.auth.*;
import com.zippendo.sdk.models.*;
import com.zippendo.sdk.api.CarriersApi;
import com.zippendo.sdk.api.CarriersApi.*;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.zippendo.com");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        CarriersApi apiInstance = new CarriersApi(defaultClient);
        String orgId = "org_01HZX9K2QF"; // String | Organization ID
        String carrierId = "carr_01HZX9K2QF"; // String | Carrier ID
        try {
            APIdisconnectCarrierRequest request = APIdisconnectCarrierRequest.newBuilder()
                .orgId(orgId)
                .carrierId(carrierId)
                .build();
            String result = apiInstance.disconnectCarrier(request);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling CarriersApi#disconnectCarrier");
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
| disconnectCarrierRequest | [**APIdisconnectCarrierRequest**](CarriersApi.md#APIdisconnectCarrierRequest)|-|-|

### Return type

**String**


### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **204** | Default Response |  -  |
| **403** | Default Response |  -  |
| **404** | Default Response |  -  |

## disconnectCarrierWithHttpInfo

> ApiResponse<String> disconnectCarrierWithHttpInfo(disconnectCarrierRequest)

Disconnect carrier

Disconnects a carrier from the organization.

### Example

```java
// Import classes:
import com.zippendo.sdk.ApiClient;
import com.zippendo.sdk.ApiException;
import com.zippendo.sdk.ApiResponse;
import com.zippendo.sdk.Configuration;
import com.zippendo.sdk.auth.*;
import com.zippendo.sdk.models.*;
import com.zippendo.sdk.api.CarriersApi;
import com.zippendo.sdk.api.CarriersApi.*;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.zippendo.com");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        CarriersApi apiInstance = new CarriersApi(defaultClient);
        String orgId = "org_01HZX9K2QF"; // String | Organization ID
        String carrierId = "carr_01HZX9K2QF"; // String | Carrier ID
        try {
            APIdisconnectCarrierRequest request = APIdisconnectCarrierRequest.newBuilder()
                .orgId(orgId)
                .carrierId(carrierId)
                .build();
            ApiResponse<String> response = apiInstance.disconnectCarrierWithHttpInfo(request);
            System.out.println("Status code: " + response.getStatusCode());
            System.out.println("Response headers: " + response.getHeaders());
            System.out.println("Response body: " + response.getData());
        } catch (ApiException e) {
            System.err.println("Exception when calling CarriersApi#disconnectCarrier");
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
| disconnectCarrierRequest | [**APIdisconnectCarrierRequest**](CarriersApi.md#APIdisconnectCarrierRequest)|-|-|

### Return type

ApiResponse<**String**>


### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **204** | Default Response |  -  |
| **403** | Default Response |  -  |
| **404** | Default Response |  -  |


<a id="APIdisconnectCarrierRequest"></a>
## APIdisconnectCarrierRequest
### Properties

|     Name      |    Type       | Description   |     Notes    |
| ------------- | ------------- | ------------- | -------------|
| **orgId** | **String** | Organization ID | |
| **carrierId** | **String** | Carrier ID | |



## getCarrier

> ListCarriers200ResponseDataInner getCarrier(getCarrierRequest)

Get carrier

Returns a single connected carrier.

### Example

```java
// Import classes:
import com.zippendo.sdk.ApiClient;
import com.zippendo.sdk.ApiException;
import com.zippendo.sdk.Configuration;
import com.zippendo.sdk.auth.*;
import com.zippendo.sdk.models.*;
import com.zippendo.sdk.api.CarriersApi;
import com.zippendo.sdk.api.CarriersApi.*;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.zippendo.com");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        CarriersApi apiInstance = new CarriersApi(defaultClient);
        String orgId = "org_01HZX9K2QF"; // String | Organization ID
        String carrierId = "carr_01HZX9K2QF"; // String | Carrier ID
        try {
            APIgetCarrierRequest request = APIgetCarrierRequest.newBuilder()
                .orgId(orgId)
                .carrierId(carrierId)
                .build();
            ListCarriers200ResponseDataInner result = apiInstance.getCarrier(request);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling CarriersApi#getCarrier");
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
| getCarrierRequest | [**APIgetCarrierRequest**](CarriersApi.md#APIgetCarrierRequest)|-|-|

### Return type

[**ListCarriers200ResponseDataInner**](ListCarriers200ResponseDataInner.md)


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

## getCarrierWithHttpInfo

> ApiResponse<ListCarriers200ResponseDataInner> getCarrierWithHttpInfo(getCarrierRequest)

Get carrier

Returns a single connected carrier.

### Example

```java
// Import classes:
import com.zippendo.sdk.ApiClient;
import com.zippendo.sdk.ApiException;
import com.zippendo.sdk.ApiResponse;
import com.zippendo.sdk.Configuration;
import com.zippendo.sdk.auth.*;
import com.zippendo.sdk.models.*;
import com.zippendo.sdk.api.CarriersApi;
import com.zippendo.sdk.api.CarriersApi.*;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.zippendo.com");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        CarriersApi apiInstance = new CarriersApi(defaultClient);
        String orgId = "org_01HZX9K2QF"; // String | Organization ID
        String carrierId = "carr_01HZX9K2QF"; // String | Carrier ID
        try {
            APIgetCarrierRequest request = APIgetCarrierRequest.newBuilder()
                .orgId(orgId)
                .carrierId(carrierId)
                .build();
            ApiResponse<ListCarriers200ResponseDataInner> response = apiInstance.getCarrierWithHttpInfo(request);
            System.out.println("Status code: " + response.getStatusCode());
            System.out.println("Response headers: " + response.getHeaders());
            System.out.println("Response body: " + response.getData());
        } catch (ApiException e) {
            System.err.println("Exception when calling CarriersApi#getCarrier");
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
| getCarrierRequest | [**APIgetCarrierRequest**](CarriersApi.md#APIgetCarrierRequest)|-|-|

### Return type

ApiResponse<[**ListCarriers200ResponseDataInner**](ListCarriers200ResponseDataInner.md)>


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


<a id="APIgetCarrierRequest"></a>
## APIgetCarrierRequest
### Properties

|     Name      |    Type       | Description   |     Notes    |
| ------------- | ------------- | ------------- | -------------|
| **orgId** | **String** | Organization ID | |
| **carrierId** | **String** | Carrier ID | |



## listCarrierProductServicePoints

> List<ListCarrierProductServicePoints200ResponseInner> listCarrierProductServicePoints(listCarrierProductServicePointsRequest)

List product service points

Returns pickup service points near a location for a specific carrier product.

### Example

```java
// Import classes:
import com.zippendo.sdk.ApiClient;
import com.zippendo.sdk.ApiException;
import com.zippendo.sdk.Configuration;
import com.zippendo.sdk.auth.*;
import com.zippendo.sdk.models.*;
import com.zippendo.sdk.api.CarriersApi;
import com.zippendo.sdk.api.CarriersApi.*;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.zippendo.com");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        CarriersApi apiInstance = new CarriersApi(defaultClient);
        String orgId = "org_01HZX9K2QF"; // String | Organization ID
        String carrierId = "carr_01HZX9K2QF"; // String | Carrier ID
        String productId = "PNL13"; // String | Carrier product ID
        ListCarrierProductServicePointsRequest listCarrierProductServicePointsRequest = new ListCarrierProductServicePointsRequest(); // ListCarrierProductServicePointsRequest | 
        try {
            APIlistCarrierProductServicePointsRequest request = APIlistCarrierProductServicePointsRequest.newBuilder()
                .orgId(orgId)
                .carrierId(carrierId)
                .productId(productId)
                .listCarrierProductServicePointsRequest(listCarrierProductServicePointsRequest)
                .build();
            List<ListCarrierProductServicePoints200ResponseInner> result = apiInstance.listCarrierProductServicePoints(request);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling CarriersApi#listCarrierProductServicePoints");
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
| listCarrierProductServicePointsRequest | [**APIlistCarrierProductServicePointsRequest**](CarriersApi.md#APIlistCarrierProductServicePointsRequest)|-|-|

### Return type

[**List&lt;ListCarrierProductServicePoints200ResponseInner&gt;**](ListCarrierProductServicePoints200ResponseInner.md)


### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Default Response |  -  |
| **403** | Default Response |  -  |
| **404** | Default Response |  -  |

## listCarrierProductServicePointsWithHttpInfo

> ApiResponse<List<ListCarrierProductServicePoints200ResponseInner>> listCarrierProductServicePointsWithHttpInfo(listCarrierProductServicePointsRequest)

List product service points

Returns pickup service points near a location for a specific carrier product.

### Example

```java
// Import classes:
import com.zippendo.sdk.ApiClient;
import com.zippendo.sdk.ApiException;
import com.zippendo.sdk.ApiResponse;
import com.zippendo.sdk.Configuration;
import com.zippendo.sdk.auth.*;
import com.zippendo.sdk.models.*;
import com.zippendo.sdk.api.CarriersApi;
import com.zippendo.sdk.api.CarriersApi.*;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.zippendo.com");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        CarriersApi apiInstance = new CarriersApi(defaultClient);
        String orgId = "org_01HZX9K2QF"; // String | Organization ID
        String carrierId = "carr_01HZX9K2QF"; // String | Carrier ID
        String productId = "PNL13"; // String | Carrier product ID
        ListCarrierProductServicePointsRequest listCarrierProductServicePointsRequest = new ListCarrierProductServicePointsRequest(); // ListCarrierProductServicePointsRequest | 
        try {
            APIlistCarrierProductServicePointsRequest request = APIlistCarrierProductServicePointsRequest.newBuilder()
                .orgId(orgId)
                .carrierId(carrierId)
                .productId(productId)
                .listCarrierProductServicePointsRequest(listCarrierProductServicePointsRequest)
                .build();
            ApiResponse<List<ListCarrierProductServicePoints200ResponseInner>> response = apiInstance.listCarrierProductServicePointsWithHttpInfo(request);
            System.out.println("Status code: " + response.getStatusCode());
            System.out.println("Response headers: " + response.getHeaders());
            System.out.println("Response body: " + response.getData());
        } catch (ApiException e) {
            System.err.println("Exception when calling CarriersApi#listCarrierProductServicePoints");
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
| listCarrierProductServicePointsRequest | [**APIlistCarrierProductServicePointsRequest**](CarriersApi.md#APIlistCarrierProductServicePointsRequest)|-|-|

### Return type

ApiResponse<[**List&lt;ListCarrierProductServicePoints200ResponseInner&gt;**](ListCarrierProductServicePoints200ResponseInner.md)>


### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Default Response |  -  |
| **403** | Default Response |  -  |
| **404** | Default Response |  -  |


<a id="APIlistCarrierProductServicePointsRequest"></a>
## APIlistCarrierProductServicePointsRequest
### Properties

|     Name      |    Type       | Description   |     Notes    |
| ------------- | ------------- | ------------- | -------------|
| **orgId** | **String** | Organization ID | |
| **carrierId** | **String** | Carrier ID | |
| **productId** | **String** | Carrier product ID | |
| **listCarrierProductServicePointsRequest** | [**ListCarrierProductServicePointsRequest**](ListCarrierProductServicePointsRequest.md) |  | |



## listCarrierProducts

> List<ListCarrierProducts200ResponseInner> listCarrierProducts(listCarrierProductsRequest)

List carrier products

Returns the carrier products available for a connected carrier.

### Example

```java
// Import classes:
import com.zippendo.sdk.ApiClient;
import com.zippendo.sdk.ApiException;
import com.zippendo.sdk.Configuration;
import com.zippendo.sdk.auth.*;
import com.zippendo.sdk.models.*;
import com.zippendo.sdk.api.CarriersApi;
import com.zippendo.sdk.api.CarriersApi.*;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.zippendo.com");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        CarriersApi apiInstance = new CarriersApi(defaultClient);
        String orgId = "org_01HZX9K2QF"; // String | Organization ID
        String carrierId = "carr_01HZX9K2QF"; // String | Carrier ID
        try {
            APIlistCarrierProductsRequest request = APIlistCarrierProductsRequest.newBuilder()
                .orgId(orgId)
                .carrierId(carrierId)
                .build();
            List<ListCarrierProducts200ResponseInner> result = apiInstance.listCarrierProducts(request);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling CarriersApi#listCarrierProducts");
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
| listCarrierProductsRequest | [**APIlistCarrierProductsRequest**](CarriersApi.md#APIlistCarrierProductsRequest)|-|-|

### Return type

[**List&lt;ListCarrierProducts200ResponseInner&gt;**](ListCarrierProducts200ResponseInner.md)


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

## listCarrierProductsWithHttpInfo

> ApiResponse<List<ListCarrierProducts200ResponseInner>> listCarrierProductsWithHttpInfo(listCarrierProductsRequest)

List carrier products

Returns the carrier products available for a connected carrier.

### Example

```java
// Import classes:
import com.zippendo.sdk.ApiClient;
import com.zippendo.sdk.ApiException;
import com.zippendo.sdk.ApiResponse;
import com.zippendo.sdk.Configuration;
import com.zippendo.sdk.auth.*;
import com.zippendo.sdk.models.*;
import com.zippendo.sdk.api.CarriersApi;
import com.zippendo.sdk.api.CarriersApi.*;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.zippendo.com");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        CarriersApi apiInstance = new CarriersApi(defaultClient);
        String orgId = "org_01HZX9K2QF"; // String | Organization ID
        String carrierId = "carr_01HZX9K2QF"; // String | Carrier ID
        try {
            APIlistCarrierProductsRequest request = APIlistCarrierProductsRequest.newBuilder()
                .orgId(orgId)
                .carrierId(carrierId)
                .build();
            ApiResponse<List<ListCarrierProducts200ResponseInner>> response = apiInstance.listCarrierProductsWithHttpInfo(request);
            System.out.println("Status code: " + response.getStatusCode());
            System.out.println("Response headers: " + response.getHeaders());
            System.out.println("Response body: " + response.getData());
        } catch (ApiException e) {
            System.err.println("Exception when calling CarriersApi#listCarrierProducts");
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
| listCarrierProductsRequest | [**APIlistCarrierProductsRequest**](CarriersApi.md#APIlistCarrierProductsRequest)|-|-|

### Return type

ApiResponse<[**List&lt;ListCarrierProducts200ResponseInner&gt;**](ListCarrierProducts200ResponseInner.md)>


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


<a id="APIlistCarrierProductsRequest"></a>
## APIlistCarrierProductsRequest
### Properties

|     Name      |    Type       | Description   |     Notes    |
| ------------- | ------------- | ------------- | -------------|
| **orgId** | **String** | Organization ID | |
| **carrierId** | **String** | Carrier ID | |



## listCarriers

> ListCarriers200Response listCarriers(listCarriersRequest)

List carriers

Returns a paginated list of carriers connected to the organization.

### Example

```java
// Import classes:
import com.zippendo.sdk.ApiClient;
import com.zippendo.sdk.ApiException;
import com.zippendo.sdk.Configuration;
import com.zippendo.sdk.auth.*;
import com.zippendo.sdk.models.*;
import com.zippendo.sdk.api.CarriersApi;
import com.zippendo.sdk.api.CarriersApi.*;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.zippendo.com");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        CarriersApi apiInstance = new CarriersApi(defaultClient);
        String orgId = "org_01HZX9K2QF"; // String | Organization ID
        Integer page = 1; // Integer | Page number (1-based)
        Integer limit = 20; // Integer | Items per page (max 100)
        String brandId = "brnd_8f3kd92ld0"; // String | Filter by brand. Pass a brand ID, or \"none\" for records not assigned to any brand.
        String brandScope = "own"; // String | How the brand context narrows this list: \"own\" returns only rows assigned to the current brand (requires a brand session, a brand-bound token, or the X-Zippendo-Brand header), \"shared\" returns only unassigned organization-wide rows, \"both\" (default) returns both. The X-Zippendo-Brand-Scope header supplies a default when the parameter is omitted. For strictly brand-owned records (orders, shipments), a brand-scoped request combined with \"shared\" returns no rows, since those records are never visible organization-wide from within a brand context.
        String carrierSlug = "gls"; // String | Filter by carrier slug.
        String search = "PostNord"; // String | Search by carrier name.
        try {
            APIlistCarriersRequest request = APIlistCarriersRequest.newBuilder()
                .orgId(orgId)
                .page(page)
                .limit(limit)
                .brandId(brandId)
                .brandScope(brandScope)
                .carrierSlug(carrierSlug)
                .search(search)
                .build();
            ListCarriers200Response result = apiInstance.listCarriers(request);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling CarriersApi#listCarriers");
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
| listCarriersRequest | [**APIlistCarriersRequest**](CarriersApi.md#APIlistCarriersRequest)|-|-|

### Return type

[**ListCarriers200Response**](ListCarriers200Response.md)


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

## listCarriersWithHttpInfo

> ApiResponse<ListCarriers200Response> listCarriersWithHttpInfo(listCarriersRequest)

List carriers

Returns a paginated list of carriers connected to the organization.

### Example

```java
// Import classes:
import com.zippendo.sdk.ApiClient;
import com.zippendo.sdk.ApiException;
import com.zippendo.sdk.ApiResponse;
import com.zippendo.sdk.Configuration;
import com.zippendo.sdk.auth.*;
import com.zippendo.sdk.models.*;
import com.zippendo.sdk.api.CarriersApi;
import com.zippendo.sdk.api.CarriersApi.*;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.zippendo.com");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        CarriersApi apiInstance = new CarriersApi(defaultClient);
        String orgId = "org_01HZX9K2QF"; // String | Organization ID
        Integer page = 1; // Integer | Page number (1-based)
        Integer limit = 20; // Integer | Items per page (max 100)
        String brandId = "brnd_8f3kd92ld0"; // String | Filter by brand. Pass a brand ID, or \"none\" for records not assigned to any brand.
        String brandScope = "own"; // String | How the brand context narrows this list: \"own\" returns only rows assigned to the current brand (requires a brand session, a brand-bound token, or the X-Zippendo-Brand header), \"shared\" returns only unassigned organization-wide rows, \"both\" (default) returns both. The X-Zippendo-Brand-Scope header supplies a default when the parameter is omitted. For strictly brand-owned records (orders, shipments), a brand-scoped request combined with \"shared\" returns no rows, since those records are never visible organization-wide from within a brand context.
        String carrierSlug = "gls"; // String | Filter by carrier slug.
        String search = "PostNord"; // String | Search by carrier name.
        try {
            APIlistCarriersRequest request = APIlistCarriersRequest.newBuilder()
                .orgId(orgId)
                .page(page)
                .limit(limit)
                .brandId(brandId)
                .brandScope(brandScope)
                .carrierSlug(carrierSlug)
                .search(search)
                .build();
            ApiResponse<ListCarriers200Response> response = apiInstance.listCarriersWithHttpInfo(request);
            System.out.println("Status code: " + response.getStatusCode());
            System.out.println("Response headers: " + response.getHeaders());
            System.out.println("Response body: " + response.getData());
        } catch (ApiException e) {
            System.err.println("Exception when calling CarriersApi#listCarriers");
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
| listCarriersRequest | [**APIlistCarriersRequest**](CarriersApi.md#APIlistCarriersRequest)|-|-|

### Return type

ApiResponse<[**ListCarriers200Response**](ListCarriers200Response.md)>


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


<a id="APIlistCarriersRequest"></a>
## APIlistCarriersRequest
### Properties

|     Name      |    Type       | Description   |     Notes    |
| ------------- | ------------- | ------------- | -------------|
| **orgId** | **String** | Organization ID | |
| **page** | **Integer** | Page number (1-based) | [optional] [default to 1] |
| **limit** | **Integer** | Items per page (max 100) | [optional] [default to 20] |
| **brandId** | **String** | Filter by brand. Pass a brand ID, or \&quot;none\&quot; for records not assigned to any brand. | [optional] |
| **brandScope** | **String** | How the brand context narrows this list: \&quot;own\&quot; returns only rows assigned to the current brand (requires a brand session, a brand-bound token, or the X-Zippendo-Brand header), \&quot;shared\&quot; returns only unassigned organization-wide rows, \&quot;both\&quot; (default) returns both. The X-Zippendo-Brand-Scope header supplies a default when the parameter is omitted. For strictly brand-owned records (orders, shipments), a brand-scoped request combined with \&quot;shared\&quot; returns no rows, since those records are never visible organization-wide from within a brand context. | [optional] [enum: own, shared, both] |
| **carrierSlug** | **String** | Filter by carrier slug. | [optional] |
| **search** | **String** | Search by carrier name. | [optional] |



## updateCarrier

> ListCarriers200ResponseDataInner updateCarrier(updateCarrierRequest)

Update carrier

Updates a connected carrier&#39;s configuration or name.

### Example

```java
// Import classes:
import com.zippendo.sdk.ApiClient;
import com.zippendo.sdk.ApiException;
import com.zippendo.sdk.Configuration;
import com.zippendo.sdk.auth.*;
import com.zippendo.sdk.models.*;
import com.zippendo.sdk.api.CarriersApi;
import com.zippendo.sdk.api.CarriersApi.*;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.zippendo.com");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        CarriersApi apiInstance = new CarriersApi(defaultClient);
        String orgId = "org_01HZX9K2QF"; // String | Organization ID
        String carrierId = "carr_01HZX9K2QF"; // String | Carrier ID
        UpdateCarrierRequest updateCarrierRequest = new UpdateCarrierRequest(); // UpdateCarrierRequest | 
        try {
            APIupdateCarrierRequest request = APIupdateCarrierRequest.newBuilder()
                .orgId(orgId)
                .carrierId(carrierId)
                .updateCarrierRequest(updateCarrierRequest)
                .build();
            ListCarriers200ResponseDataInner result = apiInstance.updateCarrier(request);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling CarriersApi#updateCarrier");
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
| updateCarrierRequest | [**APIupdateCarrierRequest**](CarriersApi.md#APIupdateCarrierRequest)|-|-|

### Return type

[**ListCarriers200ResponseDataInner**](ListCarriers200ResponseDataInner.md)


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

## updateCarrierWithHttpInfo

> ApiResponse<ListCarriers200ResponseDataInner> updateCarrierWithHttpInfo(updateCarrierRequest)

Update carrier

Updates a connected carrier&#39;s configuration or name.

### Example

```java
// Import classes:
import com.zippendo.sdk.ApiClient;
import com.zippendo.sdk.ApiException;
import com.zippendo.sdk.ApiResponse;
import com.zippendo.sdk.Configuration;
import com.zippendo.sdk.auth.*;
import com.zippendo.sdk.models.*;
import com.zippendo.sdk.api.CarriersApi;
import com.zippendo.sdk.api.CarriersApi.*;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.zippendo.com");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        CarriersApi apiInstance = new CarriersApi(defaultClient);
        String orgId = "org_01HZX9K2QF"; // String | Organization ID
        String carrierId = "carr_01HZX9K2QF"; // String | Carrier ID
        UpdateCarrierRequest updateCarrierRequest = new UpdateCarrierRequest(); // UpdateCarrierRequest | 
        try {
            APIupdateCarrierRequest request = APIupdateCarrierRequest.newBuilder()
                .orgId(orgId)
                .carrierId(carrierId)
                .updateCarrierRequest(updateCarrierRequest)
                .build();
            ApiResponse<ListCarriers200ResponseDataInner> response = apiInstance.updateCarrierWithHttpInfo(request);
            System.out.println("Status code: " + response.getStatusCode());
            System.out.println("Response headers: " + response.getHeaders());
            System.out.println("Response body: " + response.getData());
        } catch (ApiException e) {
            System.err.println("Exception when calling CarriersApi#updateCarrier");
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
| updateCarrierRequest | [**APIupdateCarrierRequest**](CarriersApi.md#APIupdateCarrierRequest)|-|-|

### Return type

ApiResponse<[**ListCarriers200ResponseDataInner**](ListCarriers200ResponseDataInner.md)>


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


<a id="APIupdateCarrierRequest"></a>
## APIupdateCarrierRequest
### Properties

|     Name      |    Type       | Description   |     Notes    |
| ------------- | ------------- | ------------- | -------------|
| **orgId** | **String** | Organization ID | |
| **carrierId** | **String** | Carrier ID | |
| **updateCarrierRequest** | [**UpdateCarrierRequest**](UpdateCarrierRequest.md) |  | |


