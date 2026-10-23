# WebhooksApi

All URIs are relative to *https://api.zippendo.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**createOrgWebhook**](WebhooksApi.md#createOrgWebhook) | **POST** /orgs/{orgId}/webhooks | Create webhook |
| [**createOrgWebhookWithHttpInfo**](WebhooksApi.md#createOrgWebhookWithHttpInfo) | **POST** /orgs/{orgId}/webhooks | Create webhook |
| [**deleteOrgWebhook**](WebhooksApi.md#deleteOrgWebhook) | **DELETE** /orgs/{orgId}/webhooks/{webhookId} | Delete webhook |
| [**deleteOrgWebhookWithHttpInfo**](WebhooksApi.md#deleteOrgWebhookWithHttpInfo) | **DELETE** /orgs/{orgId}/webhooks/{webhookId} | Delete webhook |
| [**getOrgWebhook**](WebhooksApi.md#getOrgWebhook) | **GET** /orgs/{orgId}/webhooks/{webhookId} | Get webhook |
| [**getOrgWebhookWithHttpInfo**](WebhooksApi.md#getOrgWebhookWithHttpInfo) | **GET** /orgs/{orgId}/webhooks/{webhookId} | Get webhook |
| [**listOrgWebhookDeliveries**](WebhooksApi.md#listOrgWebhookDeliveries) | **GET** /orgs/{orgId}/webhooks/{webhookId}/deliveries | List webhook deliveries |
| [**listOrgWebhookDeliveriesWithHttpInfo**](WebhooksApi.md#listOrgWebhookDeliveriesWithHttpInfo) | **GET** /orgs/{orgId}/webhooks/{webhookId}/deliveries | List webhook deliveries |
| [**listOrgWebhooks**](WebhooksApi.md#listOrgWebhooks) | **GET** /orgs/{orgId}/webhooks | List webhooks |
| [**listOrgWebhooksWithHttpInfo**](WebhooksApi.md#listOrgWebhooksWithHttpInfo) | **GET** /orgs/{orgId}/webhooks | List webhooks |
| [**testOrgWebhook**](WebhooksApi.md#testOrgWebhook) | **POST** /orgs/{orgId}/webhooks/{webhookId}/test | Test webhook |
| [**testOrgWebhookWithHttpInfo**](WebhooksApi.md#testOrgWebhookWithHttpInfo) | **POST** /orgs/{orgId}/webhooks/{webhookId}/test | Test webhook |
| [**updateOrgWebhook**](WebhooksApi.md#updateOrgWebhook) | **PATCH** /orgs/{orgId}/webhooks/{webhookId} | Update webhook |
| [**updateOrgWebhookWithHttpInfo**](WebhooksApi.md#updateOrgWebhookWithHttpInfo) | **PATCH** /orgs/{orgId}/webhooks/{webhookId} | Update webhook |



## createOrgWebhook

> CreateOrgWebhook201Response createOrgWebhook(createOrgWebhookRequest)

Create webhook

Create a new webhook endpoint for an organization that receives event notifications.

### Example

```java
// Import classes:
import com.zippendo.sdk.ApiClient;
import com.zippendo.sdk.ApiException;
import com.zippendo.sdk.Configuration;
import com.zippendo.sdk.auth.*;
import com.zippendo.sdk.models.*;
import com.zippendo.sdk.api.WebhooksApi;
import com.zippendo.sdk.api.WebhooksApi.*;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.zippendo.com");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        WebhooksApi apiInstance = new WebhooksApi(defaultClient);
        String orgId = "org_8f3kd92ld0"; // String | Organization ID
        CreateOrgWebhookRequest createOrgWebhookRequest = new CreateOrgWebhookRequest(); // CreateOrgWebhookRequest | 
        try {
            APIcreateOrgWebhookRequest request = APIcreateOrgWebhookRequest.newBuilder()
                .orgId(orgId)
                .createOrgWebhookRequest(createOrgWebhookRequest)
                .build();
            CreateOrgWebhook201Response result = apiInstance.createOrgWebhook(request);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling WebhooksApi#createOrgWebhook");
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
| createOrgWebhookRequest | [**APIcreateOrgWebhookRequest**](WebhooksApi.md#APIcreateOrgWebhookRequest)|-|-|

### Return type

[**CreateOrgWebhook201Response**](CreateOrgWebhook201Response.md)


### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Default Response |  -  |
| **401** | Default Response |  -  |
| **403** | Default Response |  -  |
| **404** | Default Response |  -  |

## createOrgWebhookWithHttpInfo

> ApiResponse<CreateOrgWebhook201Response> createOrgWebhookWithHttpInfo(createOrgWebhookRequest)

Create webhook

Create a new webhook endpoint for an organization that receives event notifications.

### Example

```java
// Import classes:
import com.zippendo.sdk.ApiClient;
import com.zippendo.sdk.ApiException;
import com.zippendo.sdk.ApiResponse;
import com.zippendo.sdk.Configuration;
import com.zippendo.sdk.auth.*;
import com.zippendo.sdk.models.*;
import com.zippendo.sdk.api.WebhooksApi;
import com.zippendo.sdk.api.WebhooksApi.*;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.zippendo.com");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        WebhooksApi apiInstance = new WebhooksApi(defaultClient);
        String orgId = "org_8f3kd92ld0"; // String | Organization ID
        CreateOrgWebhookRequest createOrgWebhookRequest = new CreateOrgWebhookRequest(); // CreateOrgWebhookRequest | 
        try {
            APIcreateOrgWebhookRequest request = APIcreateOrgWebhookRequest.newBuilder()
                .orgId(orgId)
                .createOrgWebhookRequest(createOrgWebhookRequest)
                .build();
            ApiResponse<CreateOrgWebhook201Response> response = apiInstance.createOrgWebhookWithHttpInfo(request);
            System.out.println("Status code: " + response.getStatusCode());
            System.out.println("Response headers: " + response.getHeaders());
            System.out.println("Response body: " + response.getData());
        } catch (ApiException e) {
            System.err.println("Exception when calling WebhooksApi#createOrgWebhook");
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
| createOrgWebhookRequest | [**APIcreateOrgWebhookRequest**](WebhooksApi.md#APIcreateOrgWebhookRequest)|-|-|

### Return type

ApiResponse<[**CreateOrgWebhook201Response**](CreateOrgWebhook201Response.md)>


### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Default Response |  -  |
| **401** | Default Response |  -  |
| **403** | Default Response |  -  |
| **404** | Default Response |  -  |


<a id="APIcreateOrgWebhookRequest"></a>
## APIcreateOrgWebhookRequest
### Properties

|     Name      |    Type       | Description   |     Notes    |
| ------------- | ------------- | ------------- | -------------|
| **orgId** | **String** | Organization ID | |
| **createOrgWebhookRequest** | [**CreateOrgWebhookRequest**](CreateOrgWebhookRequest.md) |  | |



## deleteOrgWebhook

> DeleteOrgWebhook200Response deleteOrgWebhook(deleteOrgWebhookRequest)

Delete webhook

Permanently delete a webhook and all its delivery logs.

### Example

```java
// Import classes:
import com.zippendo.sdk.ApiClient;
import com.zippendo.sdk.ApiException;
import com.zippendo.sdk.Configuration;
import com.zippendo.sdk.auth.*;
import com.zippendo.sdk.models.*;
import com.zippendo.sdk.api.WebhooksApi;
import com.zippendo.sdk.api.WebhooksApi.*;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.zippendo.com");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        WebhooksApi apiInstance = new WebhooksApi(defaultClient);
        String orgId = "org_clx1a2b3c4"; // String | Organization ID
        String webhookId = "wh_clx1a2b3c4"; // String | Webhook ID
        try {
            APIdeleteOrgWebhookRequest request = APIdeleteOrgWebhookRequest.newBuilder()
                .orgId(orgId)
                .webhookId(webhookId)
                .build();
            DeleteOrgWebhook200Response result = apiInstance.deleteOrgWebhook(request);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling WebhooksApi#deleteOrgWebhook");
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
| deleteOrgWebhookRequest | [**APIdeleteOrgWebhookRequest**](WebhooksApi.md#APIdeleteOrgWebhookRequest)|-|-|

### Return type

[**DeleteOrgWebhook200Response**](DeleteOrgWebhook200Response.md)


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
| **404** | Default Response |  -  |

## deleteOrgWebhookWithHttpInfo

> ApiResponse<DeleteOrgWebhook200Response> deleteOrgWebhookWithHttpInfo(deleteOrgWebhookRequest)

Delete webhook

Permanently delete a webhook and all its delivery logs.

### Example

```java
// Import classes:
import com.zippendo.sdk.ApiClient;
import com.zippendo.sdk.ApiException;
import com.zippendo.sdk.ApiResponse;
import com.zippendo.sdk.Configuration;
import com.zippendo.sdk.auth.*;
import com.zippendo.sdk.models.*;
import com.zippendo.sdk.api.WebhooksApi;
import com.zippendo.sdk.api.WebhooksApi.*;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.zippendo.com");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        WebhooksApi apiInstance = new WebhooksApi(defaultClient);
        String orgId = "org_clx1a2b3c4"; // String | Organization ID
        String webhookId = "wh_clx1a2b3c4"; // String | Webhook ID
        try {
            APIdeleteOrgWebhookRequest request = APIdeleteOrgWebhookRequest.newBuilder()
                .orgId(orgId)
                .webhookId(webhookId)
                .build();
            ApiResponse<DeleteOrgWebhook200Response> response = apiInstance.deleteOrgWebhookWithHttpInfo(request);
            System.out.println("Status code: " + response.getStatusCode());
            System.out.println("Response headers: " + response.getHeaders());
            System.out.println("Response body: " + response.getData());
        } catch (ApiException e) {
            System.err.println("Exception when calling WebhooksApi#deleteOrgWebhook");
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
| deleteOrgWebhookRequest | [**APIdeleteOrgWebhookRequest**](WebhooksApi.md#APIdeleteOrgWebhookRequest)|-|-|

### Return type

ApiResponse<[**DeleteOrgWebhook200Response**](DeleteOrgWebhook200Response.md)>


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
| **404** | Default Response |  -  |


<a id="APIdeleteOrgWebhookRequest"></a>
## APIdeleteOrgWebhookRequest
### Properties

|     Name      |    Type       | Description   |     Notes    |
| ------------- | ------------- | ------------- | -------------|
| **orgId** | **String** | Organization ID | |
| **webhookId** | **String** | Webhook ID | |



## getOrgWebhook

> CreateOrgWebhook201Response getOrgWebhook(getOrgWebhookRequest)

Get webhook

Get a specific webhook including its signing secret.

### Example

```java
// Import classes:
import com.zippendo.sdk.ApiClient;
import com.zippendo.sdk.ApiException;
import com.zippendo.sdk.Configuration;
import com.zippendo.sdk.auth.*;
import com.zippendo.sdk.models.*;
import com.zippendo.sdk.api.WebhooksApi;
import com.zippendo.sdk.api.WebhooksApi.*;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.zippendo.com");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        WebhooksApi apiInstance = new WebhooksApi(defaultClient);
        String orgId = "org_clx1a2b3c4"; // String | Organization ID
        String webhookId = "wh_clx1a2b3c4"; // String | Webhook ID
        try {
            APIgetOrgWebhookRequest request = APIgetOrgWebhookRequest.newBuilder()
                .orgId(orgId)
                .webhookId(webhookId)
                .build();
            CreateOrgWebhook201Response result = apiInstance.getOrgWebhook(request);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling WebhooksApi#getOrgWebhook");
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
| getOrgWebhookRequest | [**APIgetOrgWebhookRequest**](WebhooksApi.md#APIgetOrgWebhookRequest)|-|-|

### Return type

[**CreateOrgWebhook201Response**](CreateOrgWebhook201Response.md)


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
| **404** | Default Response |  -  |

## getOrgWebhookWithHttpInfo

> ApiResponse<CreateOrgWebhook201Response> getOrgWebhookWithHttpInfo(getOrgWebhookRequest)

Get webhook

Get a specific webhook including its signing secret.

### Example

```java
// Import classes:
import com.zippendo.sdk.ApiClient;
import com.zippendo.sdk.ApiException;
import com.zippendo.sdk.ApiResponse;
import com.zippendo.sdk.Configuration;
import com.zippendo.sdk.auth.*;
import com.zippendo.sdk.models.*;
import com.zippendo.sdk.api.WebhooksApi;
import com.zippendo.sdk.api.WebhooksApi.*;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.zippendo.com");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        WebhooksApi apiInstance = new WebhooksApi(defaultClient);
        String orgId = "org_clx1a2b3c4"; // String | Organization ID
        String webhookId = "wh_clx1a2b3c4"; // String | Webhook ID
        try {
            APIgetOrgWebhookRequest request = APIgetOrgWebhookRequest.newBuilder()
                .orgId(orgId)
                .webhookId(webhookId)
                .build();
            ApiResponse<CreateOrgWebhook201Response> response = apiInstance.getOrgWebhookWithHttpInfo(request);
            System.out.println("Status code: " + response.getStatusCode());
            System.out.println("Response headers: " + response.getHeaders());
            System.out.println("Response body: " + response.getData());
        } catch (ApiException e) {
            System.err.println("Exception when calling WebhooksApi#getOrgWebhook");
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
| getOrgWebhookRequest | [**APIgetOrgWebhookRequest**](WebhooksApi.md#APIgetOrgWebhookRequest)|-|-|

### Return type

ApiResponse<[**CreateOrgWebhook201Response**](CreateOrgWebhook201Response.md)>


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
| **404** | Default Response |  -  |


<a id="APIgetOrgWebhookRequest"></a>
## APIgetOrgWebhookRequest
### Properties

|     Name      |    Type       | Description   |     Notes    |
| ------------- | ------------- | ------------- | -------------|
| **orgId** | **String** | Organization ID | |
| **webhookId** | **String** | Webhook ID | |



## listOrgWebhookDeliveries

> ListOrgWebhookDeliveries200Response listOrgWebhookDeliveries(listOrgWebhookDeliveriesRequest)

List webhook deliveries

List the delivery history for a specific webhook.

### Example

```java
// Import classes:
import com.zippendo.sdk.ApiClient;
import com.zippendo.sdk.ApiException;
import com.zippendo.sdk.Configuration;
import com.zippendo.sdk.auth.*;
import com.zippendo.sdk.models.*;
import com.zippendo.sdk.api.WebhooksApi;
import com.zippendo.sdk.api.WebhooksApi.*;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.zippendo.com");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        WebhooksApi apiInstance = new WebhooksApi(defaultClient);
        String orgId = "org_clx1a2b3c4"; // String | Organization ID
        String webhookId = "wh_clx1a2b3c4"; // String | Webhook ID
        Integer page = 1; // Integer | Page number (1-based)
        Integer limit = 20; // Integer | Items per page (max 100)
        try {
            APIlistOrgWebhookDeliveriesRequest request = APIlistOrgWebhookDeliveriesRequest.newBuilder()
                .orgId(orgId)
                .webhookId(webhookId)
                .page(page)
                .limit(limit)
                .build();
            ListOrgWebhookDeliveries200Response result = apiInstance.listOrgWebhookDeliveries(request);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling WebhooksApi#listOrgWebhookDeliveries");
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
| listOrgWebhookDeliveriesRequest | [**APIlistOrgWebhookDeliveriesRequest**](WebhooksApi.md#APIlistOrgWebhookDeliveriesRequest)|-|-|

### Return type

[**ListOrgWebhookDeliveries200Response**](ListOrgWebhookDeliveries200Response.md)


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
| **404** | Default Response |  -  |

## listOrgWebhookDeliveriesWithHttpInfo

> ApiResponse<ListOrgWebhookDeliveries200Response> listOrgWebhookDeliveriesWithHttpInfo(listOrgWebhookDeliveriesRequest)

List webhook deliveries

List the delivery history for a specific webhook.

### Example

```java
// Import classes:
import com.zippendo.sdk.ApiClient;
import com.zippendo.sdk.ApiException;
import com.zippendo.sdk.ApiResponse;
import com.zippendo.sdk.Configuration;
import com.zippendo.sdk.auth.*;
import com.zippendo.sdk.models.*;
import com.zippendo.sdk.api.WebhooksApi;
import com.zippendo.sdk.api.WebhooksApi.*;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.zippendo.com");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        WebhooksApi apiInstance = new WebhooksApi(defaultClient);
        String orgId = "org_clx1a2b3c4"; // String | Organization ID
        String webhookId = "wh_clx1a2b3c4"; // String | Webhook ID
        Integer page = 1; // Integer | Page number (1-based)
        Integer limit = 20; // Integer | Items per page (max 100)
        try {
            APIlistOrgWebhookDeliveriesRequest request = APIlistOrgWebhookDeliveriesRequest.newBuilder()
                .orgId(orgId)
                .webhookId(webhookId)
                .page(page)
                .limit(limit)
                .build();
            ApiResponse<ListOrgWebhookDeliveries200Response> response = apiInstance.listOrgWebhookDeliveriesWithHttpInfo(request);
            System.out.println("Status code: " + response.getStatusCode());
            System.out.println("Response headers: " + response.getHeaders());
            System.out.println("Response body: " + response.getData());
        } catch (ApiException e) {
            System.err.println("Exception when calling WebhooksApi#listOrgWebhookDeliveries");
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
| listOrgWebhookDeliveriesRequest | [**APIlistOrgWebhookDeliveriesRequest**](WebhooksApi.md#APIlistOrgWebhookDeliveriesRequest)|-|-|

### Return type

ApiResponse<[**ListOrgWebhookDeliveries200Response**](ListOrgWebhookDeliveries200Response.md)>


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
| **404** | Default Response |  -  |


<a id="APIlistOrgWebhookDeliveriesRequest"></a>
## APIlistOrgWebhookDeliveriesRequest
### Properties

|     Name      |    Type       | Description   |     Notes    |
| ------------- | ------------- | ------------- | -------------|
| **orgId** | **String** | Organization ID | |
| **webhookId** | **String** | Webhook ID | |
| **page** | **Integer** | Page number (1-based) | [optional] [default to 1] |
| **limit** | **Integer** | Items per page (max 100) | [optional] [default to 20] |



## listOrgWebhooks

> ListOrgWebhooks200Response listOrgWebhooks(listOrgWebhooksRequest)

List webhooks

List all webhooks belonging to an organization.

### Example

```java
// Import classes:
import com.zippendo.sdk.ApiClient;
import com.zippendo.sdk.ApiException;
import com.zippendo.sdk.Configuration;
import com.zippendo.sdk.auth.*;
import com.zippendo.sdk.models.*;
import com.zippendo.sdk.api.WebhooksApi;
import com.zippendo.sdk.api.WebhooksApi.*;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.zippendo.com");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        WebhooksApi apiInstance = new WebhooksApi(defaultClient);
        String orgId = "org_8f3kd92ld0"; // String | Organization ID
        Integer page = 1; // Integer | Page number (1-based)
        Integer limit = 20; // Integer | Items per page (max 100)
        String brandId = "brnd_8f3kd92ld0"; // String | Filter by brand. Pass a brand ID, or \"none\" for records not assigned to any brand.
        String brandScope = "own"; // String | How the brand context narrows this list: \"own\" returns only rows assigned to the current brand (requires a brand session, a brand-bound token, or the X-Zippendo-Brand header), \"shared\" returns only unassigned organization-wide rows, \"both\" (default) returns both. The X-Zippendo-Brand-Scope header supplies a default when the parameter is omitted. For strictly brand-owned records (orders, shipments), a brand-scoped request combined with \"shared\" returns no rows, since those records are never visible organization-wide from within a brand context.
        String isActive = "true"; // String | Filter by active state.
        String search = "fulfilment"; // String | Search by webhook name or URL.
        try {
            APIlistOrgWebhooksRequest request = APIlistOrgWebhooksRequest.newBuilder()
                .orgId(orgId)
                .page(page)
                .limit(limit)
                .brandId(brandId)
                .brandScope(brandScope)
                .isActive(isActive)
                .search(search)
                .build();
            ListOrgWebhooks200Response result = apiInstance.listOrgWebhooks(request);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling WebhooksApi#listOrgWebhooks");
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
| listOrgWebhooksRequest | [**APIlistOrgWebhooksRequest**](WebhooksApi.md#APIlistOrgWebhooksRequest)|-|-|

### Return type

[**ListOrgWebhooks200Response**](ListOrgWebhooks200Response.md)


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

## listOrgWebhooksWithHttpInfo

> ApiResponse<ListOrgWebhooks200Response> listOrgWebhooksWithHttpInfo(listOrgWebhooksRequest)

List webhooks

List all webhooks belonging to an organization.

### Example

```java
// Import classes:
import com.zippendo.sdk.ApiClient;
import com.zippendo.sdk.ApiException;
import com.zippendo.sdk.ApiResponse;
import com.zippendo.sdk.Configuration;
import com.zippendo.sdk.auth.*;
import com.zippendo.sdk.models.*;
import com.zippendo.sdk.api.WebhooksApi;
import com.zippendo.sdk.api.WebhooksApi.*;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.zippendo.com");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        WebhooksApi apiInstance = new WebhooksApi(defaultClient);
        String orgId = "org_8f3kd92ld0"; // String | Organization ID
        Integer page = 1; // Integer | Page number (1-based)
        Integer limit = 20; // Integer | Items per page (max 100)
        String brandId = "brnd_8f3kd92ld0"; // String | Filter by brand. Pass a brand ID, or \"none\" for records not assigned to any brand.
        String brandScope = "own"; // String | How the brand context narrows this list: \"own\" returns only rows assigned to the current brand (requires a brand session, a brand-bound token, or the X-Zippendo-Brand header), \"shared\" returns only unassigned organization-wide rows, \"both\" (default) returns both. The X-Zippendo-Brand-Scope header supplies a default when the parameter is omitted. For strictly brand-owned records (orders, shipments), a brand-scoped request combined with \"shared\" returns no rows, since those records are never visible organization-wide from within a brand context.
        String isActive = "true"; // String | Filter by active state.
        String search = "fulfilment"; // String | Search by webhook name or URL.
        try {
            APIlistOrgWebhooksRequest request = APIlistOrgWebhooksRequest.newBuilder()
                .orgId(orgId)
                .page(page)
                .limit(limit)
                .brandId(brandId)
                .brandScope(brandScope)
                .isActive(isActive)
                .search(search)
                .build();
            ApiResponse<ListOrgWebhooks200Response> response = apiInstance.listOrgWebhooksWithHttpInfo(request);
            System.out.println("Status code: " + response.getStatusCode());
            System.out.println("Response headers: " + response.getHeaders());
            System.out.println("Response body: " + response.getData());
        } catch (ApiException e) {
            System.err.println("Exception when calling WebhooksApi#listOrgWebhooks");
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
| listOrgWebhooksRequest | [**APIlistOrgWebhooksRequest**](WebhooksApi.md#APIlistOrgWebhooksRequest)|-|-|

### Return type

ApiResponse<[**ListOrgWebhooks200Response**](ListOrgWebhooks200Response.md)>


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


<a id="APIlistOrgWebhooksRequest"></a>
## APIlistOrgWebhooksRequest
### Properties

|     Name      |    Type       | Description   |     Notes    |
| ------------- | ------------- | ------------- | -------------|
| **orgId** | **String** | Organization ID | |
| **page** | **Integer** | Page number (1-based) | [optional] [default to 1] |
| **limit** | **Integer** | Items per page (max 100) | [optional] [default to 20] |
| **brandId** | **String** | Filter by brand. Pass a brand ID, or \&quot;none\&quot; for records not assigned to any brand. | [optional] |
| **brandScope** | **String** | How the brand context narrows this list: \&quot;own\&quot; returns only rows assigned to the current brand (requires a brand session, a brand-bound token, or the X-Zippendo-Brand header), \&quot;shared\&quot; returns only unassigned organization-wide rows, \&quot;both\&quot; (default) returns both. The X-Zippendo-Brand-Scope header supplies a default when the parameter is omitted. For strictly brand-owned records (orders, shipments), a brand-scoped request combined with \&quot;shared\&quot; returns no rows, since those records are never visible organization-wide from within a brand context. | [optional] [enum: own, shared, both] |
| **isActive** | **String** | Filter by active state. | [optional] |
| **search** | **String** | Search by webhook name or URL. | [optional] |



## testOrgWebhook

> TestOrgWebhook200Response testOrgWebhook(testOrgWebhookRequest)

Test webhook

Send a test ping event to the webhook endpoint to verify connectivity.

### Example

```java
// Import classes:
import com.zippendo.sdk.ApiClient;
import com.zippendo.sdk.ApiException;
import com.zippendo.sdk.Configuration;
import com.zippendo.sdk.auth.*;
import com.zippendo.sdk.models.*;
import com.zippendo.sdk.api.WebhooksApi;
import com.zippendo.sdk.api.WebhooksApi.*;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.zippendo.com");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        WebhooksApi apiInstance = new WebhooksApi(defaultClient);
        String orgId = "org_clx1a2b3c4"; // String | Organization ID
        String webhookId = "wh_clx1a2b3c4"; // String | Webhook ID
        try {
            APItestOrgWebhookRequest request = APItestOrgWebhookRequest.newBuilder()
                .orgId(orgId)
                .webhookId(webhookId)
                .build();
            TestOrgWebhook200Response result = apiInstance.testOrgWebhook(request);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling WebhooksApi#testOrgWebhook");
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
| testOrgWebhookRequest | [**APItestOrgWebhookRequest**](WebhooksApi.md#APItestOrgWebhookRequest)|-|-|

### Return type

[**TestOrgWebhook200Response**](TestOrgWebhook200Response.md)


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
| **404** | Default Response |  -  |

## testOrgWebhookWithHttpInfo

> ApiResponse<TestOrgWebhook200Response> testOrgWebhookWithHttpInfo(testOrgWebhookRequest)

Test webhook

Send a test ping event to the webhook endpoint to verify connectivity.

### Example

```java
// Import classes:
import com.zippendo.sdk.ApiClient;
import com.zippendo.sdk.ApiException;
import com.zippendo.sdk.ApiResponse;
import com.zippendo.sdk.Configuration;
import com.zippendo.sdk.auth.*;
import com.zippendo.sdk.models.*;
import com.zippendo.sdk.api.WebhooksApi;
import com.zippendo.sdk.api.WebhooksApi.*;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.zippendo.com");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        WebhooksApi apiInstance = new WebhooksApi(defaultClient);
        String orgId = "org_clx1a2b3c4"; // String | Organization ID
        String webhookId = "wh_clx1a2b3c4"; // String | Webhook ID
        try {
            APItestOrgWebhookRequest request = APItestOrgWebhookRequest.newBuilder()
                .orgId(orgId)
                .webhookId(webhookId)
                .build();
            ApiResponse<TestOrgWebhook200Response> response = apiInstance.testOrgWebhookWithHttpInfo(request);
            System.out.println("Status code: " + response.getStatusCode());
            System.out.println("Response headers: " + response.getHeaders());
            System.out.println("Response body: " + response.getData());
        } catch (ApiException e) {
            System.err.println("Exception when calling WebhooksApi#testOrgWebhook");
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
| testOrgWebhookRequest | [**APItestOrgWebhookRequest**](WebhooksApi.md#APItestOrgWebhookRequest)|-|-|

### Return type

ApiResponse<[**TestOrgWebhook200Response**](TestOrgWebhook200Response.md)>


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
| **404** | Default Response |  -  |


<a id="APItestOrgWebhookRequest"></a>
## APItestOrgWebhookRequest
### Properties

|     Name      |    Type       | Description   |     Notes    |
| ------------- | ------------- | ------------- | -------------|
| **orgId** | **String** | Organization ID | |
| **webhookId** | **String** | Webhook ID | |



## updateOrgWebhook

> CreateOrgWebhook201Response updateOrgWebhook(updateOrgWebhookRequest)

Update webhook

Update the configuration of an existing webhook.

### Example

```java
// Import classes:
import com.zippendo.sdk.ApiClient;
import com.zippendo.sdk.ApiException;
import com.zippendo.sdk.Configuration;
import com.zippendo.sdk.auth.*;
import com.zippendo.sdk.models.*;
import com.zippendo.sdk.api.WebhooksApi;
import com.zippendo.sdk.api.WebhooksApi.*;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.zippendo.com");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        WebhooksApi apiInstance = new WebhooksApi(defaultClient);
        String orgId = "org_clx1a2b3c4"; // String | Organization ID
        String webhookId = "wh_clx1a2b3c4"; // String | Webhook ID
        UpdateOrgWebhookRequest updateOrgWebhookRequest = new UpdateOrgWebhookRequest(); // UpdateOrgWebhookRequest | 
        try {
            APIupdateOrgWebhookRequest request = APIupdateOrgWebhookRequest.newBuilder()
                .orgId(orgId)
                .webhookId(webhookId)
                .updateOrgWebhookRequest(updateOrgWebhookRequest)
                .build();
            CreateOrgWebhook201Response result = apiInstance.updateOrgWebhook(request);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling WebhooksApi#updateOrgWebhook");
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
| updateOrgWebhookRequest | [**APIupdateOrgWebhookRequest**](WebhooksApi.md#APIupdateOrgWebhookRequest)|-|-|

### Return type

[**CreateOrgWebhook201Response**](CreateOrgWebhook201Response.md)


### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Default Response |  -  |
| **401** | Default Response |  -  |
| **403** | Default Response |  -  |
| **404** | Default Response |  -  |

## updateOrgWebhookWithHttpInfo

> ApiResponse<CreateOrgWebhook201Response> updateOrgWebhookWithHttpInfo(updateOrgWebhookRequest)

Update webhook

Update the configuration of an existing webhook.

### Example

```java
// Import classes:
import com.zippendo.sdk.ApiClient;
import com.zippendo.sdk.ApiException;
import com.zippendo.sdk.ApiResponse;
import com.zippendo.sdk.Configuration;
import com.zippendo.sdk.auth.*;
import com.zippendo.sdk.models.*;
import com.zippendo.sdk.api.WebhooksApi;
import com.zippendo.sdk.api.WebhooksApi.*;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.zippendo.com");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        WebhooksApi apiInstance = new WebhooksApi(defaultClient);
        String orgId = "org_clx1a2b3c4"; // String | Organization ID
        String webhookId = "wh_clx1a2b3c4"; // String | Webhook ID
        UpdateOrgWebhookRequest updateOrgWebhookRequest = new UpdateOrgWebhookRequest(); // UpdateOrgWebhookRequest | 
        try {
            APIupdateOrgWebhookRequest request = APIupdateOrgWebhookRequest.newBuilder()
                .orgId(orgId)
                .webhookId(webhookId)
                .updateOrgWebhookRequest(updateOrgWebhookRequest)
                .build();
            ApiResponse<CreateOrgWebhook201Response> response = apiInstance.updateOrgWebhookWithHttpInfo(request);
            System.out.println("Status code: " + response.getStatusCode());
            System.out.println("Response headers: " + response.getHeaders());
            System.out.println("Response body: " + response.getData());
        } catch (ApiException e) {
            System.err.println("Exception when calling WebhooksApi#updateOrgWebhook");
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
| updateOrgWebhookRequest | [**APIupdateOrgWebhookRequest**](WebhooksApi.md#APIupdateOrgWebhookRequest)|-|-|

### Return type

ApiResponse<[**CreateOrgWebhook201Response**](CreateOrgWebhook201Response.md)>


### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Default Response |  -  |
| **401** | Default Response |  -  |
| **403** | Default Response |  -  |
| **404** | Default Response |  -  |


<a id="APIupdateOrgWebhookRequest"></a>
## APIupdateOrgWebhookRequest
### Properties

|     Name      |    Type       | Description   |     Notes    |
| ------------- | ------------- | ------------- | -------------|
| **orgId** | **String** | Organization ID | |
| **webhookId** | **String** | Webhook ID | |
| **updateOrgWebhookRequest** | [**UpdateOrgWebhookRequest**](UpdateOrgWebhookRequest.md) |  | |


