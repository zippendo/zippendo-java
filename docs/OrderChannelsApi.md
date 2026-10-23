# OrderChannelsApi

All URIs are relative to *https://api.zippendo.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**createOrderChannel**](OrderChannelsApi.md#createOrderChannel) | **POST** /orgs/{orgId}/order-channels | Create order channel |
| [**createOrderChannelWithHttpInfo**](OrderChannelsApi.md#createOrderChannelWithHttpInfo) | **POST** /orgs/{orgId}/order-channels | Create order channel |
| [**createOrderChannelWebhookSecret**](OrderChannelsApi.md#createOrderChannelWebhookSecret) | **POST** /orgs/{orgId}/order-channels/{channelId}/webhook-secret | Create or rotate webhook signing secret |
| [**createOrderChannelWebhookSecretWithHttpInfo**](OrderChannelsApi.md#createOrderChannelWebhookSecretWithHttpInfo) | **POST** /orgs/{orgId}/order-channels/{channelId}/webhook-secret | Create or rotate webhook signing secret |
| [**deleteOrderChannel**](OrderChannelsApi.md#deleteOrderChannel) | **DELETE** /orgs/{orgId}/order-channels/{channelId} | Delete order channel |
| [**deleteOrderChannelWithHttpInfo**](OrderChannelsApi.md#deleteOrderChannelWithHttpInfo) | **DELETE** /orgs/{orgId}/order-channels/{channelId} | Delete order channel |
| [**getOrderChannel**](OrderChannelsApi.md#getOrderChannel) | **GET** /orgs/{orgId}/order-channels/{channelId} | Get order channel |
| [**getOrderChannelWithHttpInfo**](OrderChannelsApi.md#getOrderChannelWithHttpInfo) | **GET** /orgs/{orgId}/order-channels/{channelId} | Get order channel |
| [**getOrderChannelWebhookStatus**](OrderChannelsApi.md#getOrderChannelWebhookStatus) | **GET** /orgs/{orgId}/order-channels/{channelId}/webhooks | Get channel webhook status |
| [**getOrderChannelWebhookStatusWithHttpInfo**](OrderChannelsApi.md#getOrderChannelWebhookStatusWithHttpInfo) | **GET** /orgs/{orgId}/order-channels/{channelId}/webhooks | Get channel webhook status |
| [**listOrderChannels**](OrderChannelsApi.md#listOrderChannels) | **GET** /orgs/{orgId}/order-channels | List order channels |
| [**listOrderChannelsWithHttpInfo**](OrderChannelsApi.md#listOrderChannelsWithHttpInfo) | **GET** /orgs/{orgId}/order-channels | List order channels |
| [**revokeOrderChannelWebhookSecret**](OrderChannelsApi.md#revokeOrderChannelWebhookSecret) | **DELETE** /orgs/{orgId}/order-channels/{channelId}/webhook-secret | Revoke webhook signing secret |
| [**revokeOrderChannelWebhookSecretWithHttpInfo**](OrderChannelsApi.md#revokeOrderChannelWebhookSecretWithHttpInfo) | **DELETE** /orgs/{orgId}/order-channels/{channelId}/webhook-secret | Revoke webhook signing secret |
| [**updateOrderChannel**](OrderChannelsApi.md#updateOrderChannel) | **PATCH** /orgs/{orgId}/order-channels/{channelId} | Update order channel |
| [**updateOrderChannelWithHttpInfo**](OrderChannelsApi.md#updateOrderChannelWithHttpInfo) | **PATCH** /orgs/{orgId}/order-channels/{channelId} | Update order channel |



## createOrderChannel

> ListOrderChannels200ResponseDataInner createOrderChannel(createOrderChannelRequest)

Create order channel

Creates a new order channel for an organization.

### Example

```java
// Import classes:
import com.zippendo.sdk.ApiClient;
import com.zippendo.sdk.ApiException;
import com.zippendo.sdk.Configuration;
import com.zippendo.sdk.auth.*;
import com.zippendo.sdk.models.*;
import com.zippendo.sdk.api.OrderChannelsApi;
import com.zippendo.sdk.api.OrderChannelsApi.*;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.zippendo.com");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        OrderChannelsApi apiInstance = new OrderChannelsApi(defaultClient);
        String orgId = "org_8f3kd92ld0"; // String | Organization ID
        CreateOrderChannelRequest createOrderChannelRequest = new CreateOrderChannelRequest(); // CreateOrderChannelRequest | 
        try {
            APIcreateOrderChannelRequest request = APIcreateOrderChannelRequest.newBuilder()
                .orgId(orgId)
                .createOrderChannelRequest(createOrderChannelRequest)
                .build();
            ListOrderChannels200ResponseDataInner result = apiInstance.createOrderChannel(request);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling OrderChannelsApi#createOrderChannel");
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
| createOrderChannelRequest | [**APIcreateOrderChannelRequest**](OrderChannelsApi.md#APIcreateOrderChannelRequest)|-|-|

### Return type

[**ListOrderChannels200ResponseDataInner**](ListOrderChannels200ResponseDataInner.md)


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

## createOrderChannelWithHttpInfo

> ApiResponse<ListOrderChannels200ResponseDataInner> createOrderChannelWithHttpInfo(createOrderChannelRequest)

Create order channel

Creates a new order channel for an organization.

### Example

```java
// Import classes:
import com.zippendo.sdk.ApiClient;
import com.zippendo.sdk.ApiException;
import com.zippendo.sdk.ApiResponse;
import com.zippendo.sdk.Configuration;
import com.zippendo.sdk.auth.*;
import com.zippendo.sdk.models.*;
import com.zippendo.sdk.api.OrderChannelsApi;
import com.zippendo.sdk.api.OrderChannelsApi.*;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.zippendo.com");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        OrderChannelsApi apiInstance = new OrderChannelsApi(defaultClient);
        String orgId = "org_8f3kd92ld0"; // String | Organization ID
        CreateOrderChannelRequest createOrderChannelRequest = new CreateOrderChannelRequest(); // CreateOrderChannelRequest | 
        try {
            APIcreateOrderChannelRequest request = APIcreateOrderChannelRequest.newBuilder()
                .orgId(orgId)
                .createOrderChannelRequest(createOrderChannelRequest)
                .build();
            ApiResponse<ListOrderChannels200ResponseDataInner> response = apiInstance.createOrderChannelWithHttpInfo(request);
            System.out.println("Status code: " + response.getStatusCode());
            System.out.println("Response headers: " + response.getHeaders());
            System.out.println("Response body: " + response.getData());
        } catch (ApiException e) {
            System.err.println("Exception when calling OrderChannelsApi#createOrderChannel");
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
| createOrderChannelRequest | [**APIcreateOrderChannelRequest**](OrderChannelsApi.md#APIcreateOrderChannelRequest)|-|-|

### Return type

ApiResponse<[**ListOrderChannels200ResponseDataInner**](ListOrderChannels200ResponseDataInner.md)>


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


<a id="APIcreateOrderChannelRequest"></a>
## APIcreateOrderChannelRequest
### Properties

|     Name      |    Type       | Description   |     Notes    |
| ------------- | ------------- | ------------- | -------------|
| **orgId** | **String** | Organization ID | |
| **createOrderChannelRequest** | [**CreateOrderChannelRequest**](CreateOrderChannelRequest.md) |  | |



## createOrderChannelWebhookSecret

> CreateOrderChannelWebhookSecret201Response createOrderChannelWebhookSecret(createOrderChannelWebhookSecretRequest)

Create or rotate webhook signing secret

Generates (or rotates) the custom channel&#39;s webhook signing secret used to authenticate order pushes to the ingest URL. The secret is returned only once. Rotating invalidates the previous secret immediately.

### Example

```java
// Import classes:
import com.zippendo.sdk.ApiClient;
import com.zippendo.sdk.ApiException;
import com.zippendo.sdk.Configuration;
import com.zippendo.sdk.auth.*;
import com.zippendo.sdk.models.*;
import com.zippendo.sdk.api.OrderChannelsApi;
import com.zippendo.sdk.api.OrderChannelsApi.*;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.zippendo.com");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        OrderChannelsApi apiInstance = new OrderChannelsApi(defaultClient);
        String orgId = "clz9k2f0a0000abcd0000zzzz"; // String | Organization ID.
        String channelId = "clz9k2f0a0001abcd1234efgh"; // String | Order channel ID.
        try {
            APIcreateOrderChannelWebhookSecretRequest request = APIcreateOrderChannelWebhookSecretRequest.newBuilder()
                .orgId(orgId)
                .channelId(channelId)
                .build();
            CreateOrderChannelWebhookSecret201Response result = apiInstance.createOrderChannelWebhookSecret(request);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling OrderChannelsApi#createOrderChannelWebhookSecret");
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
| createOrderChannelWebhookSecretRequest | [**APIcreateOrderChannelWebhookSecretRequest**](OrderChannelsApi.md#APIcreateOrderChannelWebhookSecretRequest)|-|-|

### Return type

[**CreateOrderChannelWebhookSecret201Response**](CreateOrderChannelWebhookSecret201Response.md)


### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Default Response |  -  |
| **400** | Default Response |  -  |
| **403** | Default Response |  -  |
| **404** | Default Response |  -  |

## createOrderChannelWebhookSecretWithHttpInfo

> ApiResponse<CreateOrderChannelWebhookSecret201Response> createOrderChannelWebhookSecretWithHttpInfo(createOrderChannelWebhookSecretRequest)

Create or rotate webhook signing secret

Generates (or rotates) the custom channel&#39;s webhook signing secret used to authenticate order pushes to the ingest URL. The secret is returned only once. Rotating invalidates the previous secret immediately.

### Example

```java
// Import classes:
import com.zippendo.sdk.ApiClient;
import com.zippendo.sdk.ApiException;
import com.zippendo.sdk.ApiResponse;
import com.zippendo.sdk.Configuration;
import com.zippendo.sdk.auth.*;
import com.zippendo.sdk.models.*;
import com.zippendo.sdk.api.OrderChannelsApi;
import com.zippendo.sdk.api.OrderChannelsApi.*;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.zippendo.com");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        OrderChannelsApi apiInstance = new OrderChannelsApi(defaultClient);
        String orgId = "clz9k2f0a0000abcd0000zzzz"; // String | Organization ID.
        String channelId = "clz9k2f0a0001abcd1234efgh"; // String | Order channel ID.
        try {
            APIcreateOrderChannelWebhookSecretRequest request = APIcreateOrderChannelWebhookSecretRequest.newBuilder()
                .orgId(orgId)
                .channelId(channelId)
                .build();
            ApiResponse<CreateOrderChannelWebhookSecret201Response> response = apiInstance.createOrderChannelWebhookSecretWithHttpInfo(request);
            System.out.println("Status code: " + response.getStatusCode());
            System.out.println("Response headers: " + response.getHeaders());
            System.out.println("Response body: " + response.getData());
        } catch (ApiException e) {
            System.err.println("Exception when calling OrderChannelsApi#createOrderChannelWebhookSecret");
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
| createOrderChannelWebhookSecretRequest | [**APIcreateOrderChannelWebhookSecretRequest**](OrderChannelsApi.md#APIcreateOrderChannelWebhookSecretRequest)|-|-|

### Return type

ApiResponse<[**CreateOrderChannelWebhookSecret201Response**](CreateOrderChannelWebhookSecret201Response.md)>


### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Default Response |  -  |
| **400** | Default Response |  -  |
| **403** | Default Response |  -  |
| **404** | Default Response |  -  |


<a id="APIcreateOrderChannelWebhookSecretRequest"></a>
## APIcreateOrderChannelWebhookSecretRequest
### Properties

|     Name      |    Type       | Description   |     Notes    |
| ------------- | ------------- | ------------- | -------------|
| **orgId** | **String** | Organization ID. | |
| **channelId** | **String** | Order channel ID. | |



## deleteOrderChannel

> RevokeApiToken200Response deleteOrderChannel(deleteOrderChannelRequest)

Delete order channel

Deletes an order channel and cascades deletion of its orders.

### Example

```java
// Import classes:
import com.zippendo.sdk.ApiClient;
import com.zippendo.sdk.ApiException;
import com.zippendo.sdk.Configuration;
import com.zippendo.sdk.auth.*;
import com.zippendo.sdk.models.*;
import com.zippendo.sdk.api.OrderChannelsApi;
import com.zippendo.sdk.api.OrderChannelsApi.*;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.zippendo.com");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        OrderChannelsApi apiInstance = new OrderChannelsApi(defaultClient);
        String orgId = "clz9k2f0a0000abcd0000zzzz"; // String | Organization ID.
        String channelId = "clz9k2f0a0001abcd1234efgh"; // String | Order channel ID.
        try {
            APIdeleteOrderChannelRequest request = APIdeleteOrderChannelRequest.newBuilder()
                .orgId(orgId)
                .channelId(channelId)
                .build();
            RevokeApiToken200Response result = apiInstance.deleteOrderChannel(request);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling OrderChannelsApi#deleteOrderChannel");
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
| deleteOrderChannelRequest | [**APIdeleteOrderChannelRequest**](OrderChannelsApi.md#APIdeleteOrderChannelRequest)|-|-|

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

## deleteOrderChannelWithHttpInfo

> ApiResponse<RevokeApiToken200Response> deleteOrderChannelWithHttpInfo(deleteOrderChannelRequest)

Delete order channel

Deletes an order channel and cascades deletion of its orders.

### Example

```java
// Import classes:
import com.zippendo.sdk.ApiClient;
import com.zippendo.sdk.ApiException;
import com.zippendo.sdk.ApiResponse;
import com.zippendo.sdk.Configuration;
import com.zippendo.sdk.auth.*;
import com.zippendo.sdk.models.*;
import com.zippendo.sdk.api.OrderChannelsApi;
import com.zippendo.sdk.api.OrderChannelsApi.*;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.zippendo.com");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        OrderChannelsApi apiInstance = new OrderChannelsApi(defaultClient);
        String orgId = "clz9k2f0a0000abcd0000zzzz"; // String | Organization ID.
        String channelId = "clz9k2f0a0001abcd1234efgh"; // String | Order channel ID.
        try {
            APIdeleteOrderChannelRequest request = APIdeleteOrderChannelRequest.newBuilder()
                .orgId(orgId)
                .channelId(channelId)
                .build();
            ApiResponse<RevokeApiToken200Response> response = apiInstance.deleteOrderChannelWithHttpInfo(request);
            System.out.println("Status code: " + response.getStatusCode());
            System.out.println("Response headers: " + response.getHeaders());
            System.out.println("Response body: " + response.getData());
        } catch (ApiException e) {
            System.err.println("Exception when calling OrderChannelsApi#deleteOrderChannel");
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
| deleteOrderChannelRequest | [**APIdeleteOrderChannelRequest**](OrderChannelsApi.md#APIdeleteOrderChannelRequest)|-|-|

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


<a id="APIdeleteOrderChannelRequest"></a>
## APIdeleteOrderChannelRequest
### Properties

|     Name      |    Type       | Description   |     Notes    |
| ------------- | ------------- | ------------- | -------------|
| **orgId** | **String** | Organization ID. | |
| **channelId** | **String** | Order channel ID. | |



## getOrderChannel

> ListOrderChannels200ResponseDataInner getOrderChannel(getOrderChannelRequest)

Get order channel

Returns a single order channel by ID, including its linked shipping rules.

### Example

```java
// Import classes:
import com.zippendo.sdk.ApiClient;
import com.zippendo.sdk.ApiException;
import com.zippendo.sdk.Configuration;
import com.zippendo.sdk.auth.*;
import com.zippendo.sdk.models.*;
import com.zippendo.sdk.api.OrderChannelsApi;
import com.zippendo.sdk.api.OrderChannelsApi.*;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.zippendo.com");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        OrderChannelsApi apiInstance = new OrderChannelsApi(defaultClient);
        String orgId = "clz9k2f0a0000abcd0000zzzz"; // String | Organization ID.
        String channelId = "clz9k2f0a0001abcd1234efgh"; // String | Order channel ID.
        try {
            APIgetOrderChannelRequest request = APIgetOrderChannelRequest.newBuilder()
                .orgId(orgId)
                .channelId(channelId)
                .build();
            ListOrderChannels200ResponseDataInner result = apiInstance.getOrderChannel(request);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling OrderChannelsApi#getOrderChannel");
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
| getOrderChannelRequest | [**APIgetOrderChannelRequest**](OrderChannelsApi.md#APIgetOrderChannelRequest)|-|-|

### Return type

[**ListOrderChannels200ResponseDataInner**](ListOrderChannels200ResponseDataInner.md)


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

## getOrderChannelWithHttpInfo

> ApiResponse<ListOrderChannels200ResponseDataInner> getOrderChannelWithHttpInfo(getOrderChannelRequest)

Get order channel

Returns a single order channel by ID, including its linked shipping rules.

### Example

```java
// Import classes:
import com.zippendo.sdk.ApiClient;
import com.zippendo.sdk.ApiException;
import com.zippendo.sdk.ApiResponse;
import com.zippendo.sdk.Configuration;
import com.zippendo.sdk.auth.*;
import com.zippendo.sdk.models.*;
import com.zippendo.sdk.api.OrderChannelsApi;
import com.zippendo.sdk.api.OrderChannelsApi.*;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.zippendo.com");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        OrderChannelsApi apiInstance = new OrderChannelsApi(defaultClient);
        String orgId = "clz9k2f0a0000abcd0000zzzz"; // String | Organization ID.
        String channelId = "clz9k2f0a0001abcd1234efgh"; // String | Order channel ID.
        try {
            APIgetOrderChannelRequest request = APIgetOrderChannelRequest.newBuilder()
                .orgId(orgId)
                .channelId(channelId)
                .build();
            ApiResponse<ListOrderChannels200ResponseDataInner> response = apiInstance.getOrderChannelWithHttpInfo(request);
            System.out.println("Status code: " + response.getStatusCode());
            System.out.println("Response headers: " + response.getHeaders());
            System.out.println("Response body: " + response.getData());
        } catch (ApiException e) {
            System.err.println("Exception when calling OrderChannelsApi#getOrderChannel");
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
| getOrderChannelRequest | [**APIgetOrderChannelRequest**](OrderChannelsApi.md#APIgetOrderChannelRequest)|-|-|

### Return type

ApiResponse<[**ListOrderChannels200ResponseDataInner**](ListOrderChannels200ResponseDataInner.md)>


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


<a id="APIgetOrderChannelRequest"></a>
## APIgetOrderChannelRequest
### Properties

|     Name      |    Type       | Description   |     Notes    |
| ------------- | ------------- | ------------- | -------------|
| **orgId** | **String** | Organization ID. | |
| **channelId** | **String** | Order channel ID. | |



## getOrderChannelWebhookStatus

> GetOrderChannelWebhookStatus200Response getOrderChannelWebhookStatus(getOrderChannelWebhookStatusRequest)

Get channel webhook status

Returns whether webhooks are enabled and lists the webhooks registered with the platform.

### Example

```java
// Import classes:
import com.zippendo.sdk.ApiClient;
import com.zippendo.sdk.ApiException;
import com.zippendo.sdk.Configuration;
import com.zippendo.sdk.auth.*;
import com.zippendo.sdk.models.*;
import com.zippendo.sdk.api.OrderChannelsApi;
import com.zippendo.sdk.api.OrderChannelsApi.*;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.zippendo.com");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        OrderChannelsApi apiInstance = new OrderChannelsApi(defaultClient);
        String orgId = "clz9k2f0a0000abcd0000zzzz"; // String | Organization ID.
        String channelId = "clz9k2f0a0001abcd1234efgh"; // String | Order channel ID.
        try {
            APIgetOrderChannelWebhookStatusRequest request = APIgetOrderChannelWebhookStatusRequest.newBuilder()
                .orgId(orgId)
                .channelId(channelId)
                .build();
            GetOrderChannelWebhookStatus200Response result = apiInstance.getOrderChannelWebhookStatus(request);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling OrderChannelsApi#getOrderChannelWebhookStatus");
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
| getOrderChannelWebhookStatusRequest | [**APIgetOrderChannelWebhookStatusRequest**](OrderChannelsApi.md#APIgetOrderChannelWebhookStatusRequest)|-|-|

### Return type

[**GetOrderChannelWebhookStatus200Response**](GetOrderChannelWebhookStatus200Response.md)


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

## getOrderChannelWebhookStatusWithHttpInfo

> ApiResponse<GetOrderChannelWebhookStatus200Response> getOrderChannelWebhookStatusWithHttpInfo(getOrderChannelWebhookStatusRequest)

Get channel webhook status

Returns whether webhooks are enabled and lists the webhooks registered with the platform.

### Example

```java
// Import classes:
import com.zippendo.sdk.ApiClient;
import com.zippendo.sdk.ApiException;
import com.zippendo.sdk.ApiResponse;
import com.zippendo.sdk.Configuration;
import com.zippendo.sdk.auth.*;
import com.zippendo.sdk.models.*;
import com.zippendo.sdk.api.OrderChannelsApi;
import com.zippendo.sdk.api.OrderChannelsApi.*;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.zippendo.com");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        OrderChannelsApi apiInstance = new OrderChannelsApi(defaultClient);
        String orgId = "clz9k2f0a0000abcd0000zzzz"; // String | Organization ID.
        String channelId = "clz9k2f0a0001abcd1234efgh"; // String | Order channel ID.
        try {
            APIgetOrderChannelWebhookStatusRequest request = APIgetOrderChannelWebhookStatusRequest.newBuilder()
                .orgId(orgId)
                .channelId(channelId)
                .build();
            ApiResponse<GetOrderChannelWebhookStatus200Response> response = apiInstance.getOrderChannelWebhookStatusWithHttpInfo(request);
            System.out.println("Status code: " + response.getStatusCode());
            System.out.println("Response headers: " + response.getHeaders());
            System.out.println("Response body: " + response.getData());
        } catch (ApiException e) {
            System.err.println("Exception when calling OrderChannelsApi#getOrderChannelWebhookStatus");
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
| getOrderChannelWebhookStatusRequest | [**APIgetOrderChannelWebhookStatusRequest**](OrderChannelsApi.md#APIgetOrderChannelWebhookStatusRequest)|-|-|

### Return type

ApiResponse<[**GetOrderChannelWebhookStatus200Response**](GetOrderChannelWebhookStatus200Response.md)>


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


<a id="APIgetOrderChannelWebhookStatusRequest"></a>
## APIgetOrderChannelWebhookStatusRequest
### Properties

|     Name      |    Type       | Description   |     Notes    |
| ------------- | ------------- | ------------- | -------------|
| **orgId** | **String** | Organization ID. | |
| **channelId** | **String** | Order channel ID. | |



## listOrderChannels

> ListOrderChannels200Response listOrderChannels(listOrderChannelsRequest)

List order channels

Returns a paginated list of order channels for an organization.

### Example

```java
// Import classes:
import com.zippendo.sdk.ApiClient;
import com.zippendo.sdk.ApiException;
import com.zippendo.sdk.Configuration;
import com.zippendo.sdk.auth.*;
import com.zippendo.sdk.models.*;
import com.zippendo.sdk.api.OrderChannelsApi;
import com.zippendo.sdk.api.OrderChannelsApi.*;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.zippendo.com");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        OrderChannelsApi apiInstance = new OrderChannelsApi(defaultClient);
        String orgId = "org_8f3kd92ld0"; // String | Organization ID
        Integer page = 1; // Integer | Page number (1-based)
        Integer limit = 20; // Integer | Items per page (max 100)
        String brandId = "brnd_8f3kd92ld0"; // String | Filter by brand. Pass a brand ID, or \"none\" for records not assigned to any brand.
        String brandScope = "own"; // String | How the brand context narrows this list: \"own\" returns only rows assigned to the current brand (requires a brand session, a brand-bound token, or the X-Zippendo-Brand header), \"shared\" returns only unassigned organization-wide rows, \"both\" (default) returns both. The X-Zippendo-Brand-Scope header supplies a default when the parameter is omitted. For strictly brand-owned records (orders, shipments), a brand-scoped request combined with \"shared\" returns no rows, since those records are never visible organization-wide from within a brand context.
        String type = "shopify"; // String | Filter by channel type.
        String enabled = "true"; // String | Filter by enabled state.
        String search = "Anna's Shopify Store"; // String | Search by channel name.
        try {
            APIlistOrderChannelsRequest request = APIlistOrderChannelsRequest.newBuilder()
                .orgId(orgId)
                .page(page)
                .limit(limit)
                .brandId(brandId)
                .brandScope(brandScope)
                .type(type)
                .enabled(enabled)
                .search(search)
                .build();
            ListOrderChannels200Response result = apiInstance.listOrderChannels(request);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling OrderChannelsApi#listOrderChannels");
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
| listOrderChannelsRequest | [**APIlistOrderChannelsRequest**](OrderChannelsApi.md#APIlistOrderChannelsRequest)|-|-|

### Return type

[**ListOrderChannels200Response**](ListOrderChannels200Response.md)


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

## listOrderChannelsWithHttpInfo

> ApiResponse<ListOrderChannels200Response> listOrderChannelsWithHttpInfo(listOrderChannelsRequest)

List order channels

Returns a paginated list of order channels for an organization.

### Example

```java
// Import classes:
import com.zippendo.sdk.ApiClient;
import com.zippendo.sdk.ApiException;
import com.zippendo.sdk.ApiResponse;
import com.zippendo.sdk.Configuration;
import com.zippendo.sdk.auth.*;
import com.zippendo.sdk.models.*;
import com.zippendo.sdk.api.OrderChannelsApi;
import com.zippendo.sdk.api.OrderChannelsApi.*;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.zippendo.com");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        OrderChannelsApi apiInstance = new OrderChannelsApi(defaultClient);
        String orgId = "org_8f3kd92ld0"; // String | Organization ID
        Integer page = 1; // Integer | Page number (1-based)
        Integer limit = 20; // Integer | Items per page (max 100)
        String brandId = "brnd_8f3kd92ld0"; // String | Filter by brand. Pass a brand ID, or \"none\" for records not assigned to any brand.
        String brandScope = "own"; // String | How the brand context narrows this list: \"own\" returns only rows assigned to the current brand (requires a brand session, a brand-bound token, or the X-Zippendo-Brand header), \"shared\" returns only unassigned organization-wide rows, \"both\" (default) returns both. The X-Zippendo-Brand-Scope header supplies a default when the parameter is omitted. For strictly brand-owned records (orders, shipments), a brand-scoped request combined with \"shared\" returns no rows, since those records are never visible organization-wide from within a brand context.
        String type = "shopify"; // String | Filter by channel type.
        String enabled = "true"; // String | Filter by enabled state.
        String search = "Anna's Shopify Store"; // String | Search by channel name.
        try {
            APIlistOrderChannelsRequest request = APIlistOrderChannelsRequest.newBuilder()
                .orgId(orgId)
                .page(page)
                .limit(limit)
                .brandId(brandId)
                .brandScope(brandScope)
                .type(type)
                .enabled(enabled)
                .search(search)
                .build();
            ApiResponse<ListOrderChannels200Response> response = apiInstance.listOrderChannelsWithHttpInfo(request);
            System.out.println("Status code: " + response.getStatusCode());
            System.out.println("Response headers: " + response.getHeaders());
            System.out.println("Response body: " + response.getData());
        } catch (ApiException e) {
            System.err.println("Exception when calling OrderChannelsApi#listOrderChannels");
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
| listOrderChannelsRequest | [**APIlistOrderChannelsRequest**](OrderChannelsApi.md#APIlistOrderChannelsRequest)|-|-|

### Return type

ApiResponse<[**ListOrderChannels200Response**](ListOrderChannels200Response.md)>


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


<a id="APIlistOrderChannelsRequest"></a>
## APIlistOrderChannelsRequest
### Properties

|     Name      |    Type       | Description   |     Notes    |
| ------------- | ------------- | ------------- | -------------|
| **orgId** | **String** | Organization ID | |
| **page** | **Integer** | Page number (1-based) | [optional] [default to 1] |
| **limit** | **Integer** | Items per page (max 100) | [optional] [default to 20] |
| **brandId** | **String** | Filter by brand. Pass a brand ID, or \&quot;none\&quot; for records not assigned to any brand. | [optional] |
| **brandScope** | **String** | How the brand context narrows this list: \&quot;own\&quot; returns only rows assigned to the current brand (requires a brand session, a brand-bound token, or the X-Zippendo-Brand header), \&quot;shared\&quot; returns only unassigned organization-wide rows, \&quot;both\&quot; (default) returns both. The X-Zippendo-Brand-Scope header supplies a default when the parameter is omitted. For strictly brand-owned records (orders, shipments), a brand-scoped request combined with \&quot;shared\&quot; returns no rows, since those records are never visible organization-wide from within a brand context. | [optional] [enum: own, shared, both] |
| **type** | **String** | Filter by channel type. | [optional] [enum: shopify, woocommerce, manual, custom] |
| **enabled** | **String** | Filter by enabled state. | [optional] |
| **search** | **String** | Search by channel name. | [optional] |



## revokeOrderChannelWebhookSecret

> RevokeOrderChannelWebhookSecret200Response revokeOrderChannelWebhookSecret(revokeOrderChannelWebhookSecretRequest)

Revoke webhook signing secret

Revokes the custom channel&#39;s webhook signing secret. All subsequent pushes to the ingest URL are rejected until a new secret is generated.

### Example

```java
// Import classes:
import com.zippendo.sdk.ApiClient;
import com.zippendo.sdk.ApiException;
import com.zippendo.sdk.Configuration;
import com.zippendo.sdk.auth.*;
import com.zippendo.sdk.models.*;
import com.zippendo.sdk.api.OrderChannelsApi;
import com.zippendo.sdk.api.OrderChannelsApi.*;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.zippendo.com");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        OrderChannelsApi apiInstance = new OrderChannelsApi(defaultClient);
        String orgId = "clz9k2f0a0000abcd0000zzzz"; // String | Organization ID.
        String channelId = "clz9k2f0a0001abcd1234efgh"; // String | Order channel ID.
        try {
            APIrevokeOrderChannelWebhookSecretRequest request = APIrevokeOrderChannelWebhookSecretRequest.newBuilder()
                .orgId(orgId)
                .channelId(channelId)
                .build();
            RevokeOrderChannelWebhookSecret200Response result = apiInstance.revokeOrderChannelWebhookSecret(request);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling OrderChannelsApi#revokeOrderChannelWebhookSecret");
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
| revokeOrderChannelWebhookSecretRequest | [**APIrevokeOrderChannelWebhookSecretRequest**](OrderChannelsApi.md#APIrevokeOrderChannelWebhookSecretRequest)|-|-|

### Return type

[**RevokeOrderChannelWebhookSecret200Response**](RevokeOrderChannelWebhookSecret200Response.md)


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

## revokeOrderChannelWebhookSecretWithHttpInfo

> ApiResponse<RevokeOrderChannelWebhookSecret200Response> revokeOrderChannelWebhookSecretWithHttpInfo(revokeOrderChannelWebhookSecretRequest)

Revoke webhook signing secret

Revokes the custom channel&#39;s webhook signing secret. All subsequent pushes to the ingest URL are rejected until a new secret is generated.

### Example

```java
// Import classes:
import com.zippendo.sdk.ApiClient;
import com.zippendo.sdk.ApiException;
import com.zippendo.sdk.ApiResponse;
import com.zippendo.sdk.Configuration;
import com.zippendo.sdk.auth.*;
import com.zippendo.sdk.models.*;
import com.zippendo.sdk.api.OrderChannelsApi;
import com.zippendo.sdk.api.OrderChannelsApi.*;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.zippendo.com");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        OrderChannelsApi apiInstance = new OrderChannelsApi(defaultClient);
        String orgId = "clz9k2f0a0000abcd0000zzzz"; // String | Organization ID.
        String channelId = "clz9k2f0a0001abcd1234efgh"; // String | Order channel ID.
        try {
            APIrevokeOrderChannelWebhookSecretRequest request = APIrevokeOrderChannelWebhookSecretRequest.newBuilder()
                .orgId(orgId)
                .channelId(channelId)
                .build();
            ApiResponse<RevokeOrderChannelWebhookSecret200Response> response = apiInstance.revokeOrderChannelWebhookSecretWithHttpInfo(request);
            System.out.println("Status code: " + response.getStatusCode());
            System.out.println("Response headers: " + response.getHeaders());
            System.out.println("Response body: " + response.getData());
        } catch (ApiException e) {
            System.err.println("Exception when calling OrderChannelsApi#revokeOrderChannelWebhookSecret");
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
| revokeOrderChannelWebhookSecretRequest | [**APIrevokeOrderChannelWebhookSecretRequest**](OrderChannelsApi.md#APIrevokeOrderChannelWebhookSecretRequest)|-|-|

### Return type

ApiResponse<[**RevokeOrderChannelWebhookSecret200Response**](RevokeOrderChannelWebhookSecret200Response.md)>


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


<a id="APIrevokeOrderChannelWebhookSecretRequest"></a>
## APIrevokeOrderChannelWebhookSecretRequest
### Properties

|     Name      |    Type       | Description   |     Notes    |
| ------------- | ------------- | ------------- | -------------|
| **orgId** | **String** | Organization ID. | |
| **channelId** | **String** | Order channel ID. | |



## updateOrderChannel

> ListOrderChannels200ResponseDataInner updateOrderChannel(updateOrderChannelRequest)

Update order channel

Updates an order channel and its linked shipping rules.

### Example

```java
// Import classes:
import com.zippendo.sdk.ApiClient;
import com.zippendo.sdk.ApiException;
import com.zippendo.sdk.Configuration;
import com.zippendo.sdk.auth.*;
import com.zippendo.sdk.models.*;
import com.zippendo.sdk.api.OrderChannelsApi;
import com.zippendo.sdk.api.OrderChannelsApi.*;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.zippendo.com");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        OrderChannelsApi apiInstance = new OrderChannelsApi(defaultClient);
        String orgId = "clz9k2f0a0000abcd0000zzzz"; // String | Organization ID.
        String channelId = "clz9k2f0a0001abcd1234efgh"; // String | Order channel ID.
        UpdateOrderChannelRequest updateOrderChannelRequest = new UpdateOrderChannelRequest(); // UpdateOrderChannelRequest | 
        try {
            APIupdateOrderChannelRequest request = APIupdateOrderChannelRequest.newBuilder()
                .orgId(orgId)
                .channelId(channelId)
                .updateOrderChannelRequest(updateOrderChannelRequest)
                .build();
            ListOrderChannels200ResponseDataInner result = apiInstance.updateOrderChannel(request);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling OrderChannelsApi#updateOrderChannel");
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
| updateOrderChannelRequest | [**APIupdateOrderChannelRequest**](OrderChannelsApi.md#APIupdateOrderChannelRequest)|-|-|

### Return type

[**ListOrderChannels200ResponseDataInner**](ListOrderChannels200ResponseDataInner.md)


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

## updateOrderChannelWithHttpInfo

> ApiResponse<ListOrderChannels200ResponseDataInner> updateOrderChannelWithHttpInfo(updateOrderChannelRequest)

Update order channel

Updates an order channel and its linked shipping rules.

### Example

```java
// Import classes:
import com.zippendo.sdk.ApiClient;
import com.zippendo.sdk.ApiException;
import com.zippendo.sdk.ApiResponse;
import com.zippendo.sdk.Configuration;
import com.zippendo.sdk.auth.*;
import com.zippendo.sdk.models.*;
import com.zippendo.sdk.api.OrderChannelsApi;
import com.zippendo.sdk.api.OrderChannelsApi.*;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.zippendo.com");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        OrderChannelsApi apiInstance = new OrderChannelsApi(defaultClient);
        String orgId = "clz9k2f0a0000abcd0000zzzz"; // String | Organization ID.
        String channelId = "clz9k2f0a0001abcd1234efgh"; // String | Order channel ID.
        UpdateOrderChannelRequest updateOrderChannelRequest = new UpdateOrderChannelRequest(); // UpdateOrderChannelRequest | 
        try {
            APIupdateOrderChannelRequest request = APIupdateOrderChannelRequest.newBuilder()
                .orgId(orgId)
                .channelId(channelId)
                .updateOrderChannelRequest(updateOrderChannelRequest)
                .build();
            ApiResponse<ListOrderChannels200ResponseDataInner> response = apiInstance.updateOrderChannelWithHttpInfo(request);
            System.out.println("Status code: " + response.getStatusCode());
            System.out.println("Response headers: " + response.getHeaders());
            System.out.println("Response body: " + response.getData());
        } catch (ApiException e) {
            System.err.println("Exception when calling OrderChannelsApi#updateOrderChannel");
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
| updateOrderChannelRequest | [**APIupdateOrderChannelRequest**](OrderChannelsApi.md#APIupdateOrderChannelRequest)|-|-|

### Return type

ApiResponse<[**ListOrderChannels200ResponseDataInner**](ListOrderChannels200ResponseDataInner.md)>


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


<a id="APIupdateOrderChannelRequest"></a>
## APIupdateOrderChannelRequest
### Properties

|     Name      |    Type       | Description   |     Notes    |
| ------------- | ------------- | ------------- | -------------|
| **orgId** | **String** | Organization ID. | |
| **channelId** | **String** | Order channel ID. | |
| **updateOrderChannelRequest** | [**UpdateOrderChannelRequest**](UpdateOrderChannelRequest.md) |  | |


