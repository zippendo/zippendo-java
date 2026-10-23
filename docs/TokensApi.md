# TokensApi

All URIs are relative to *https://api.zippendo.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**createApiToken**](TokensApi.md#createApiToken) | **POST** /orgs/{orgId}/api-tokens | Create API keys |
| [**createApiTokenWithHttpInfo**](TokensApi.md#createApiTokenWithHttpInfo) | **POST** /orgs/{orgId}/api-tokens | Create API keys |
| [**getApiToken**](TokensApi.md#getApiToken) | **GET** /orgs/{orgId}/api-tokens/{tokenId} | Get API keys |
| [**getApiTokenWithHttpInfo**](TokensApi.md#getApiTokenWithHttpInfo) | **GET** /orgs/{orgId}/api-tokens/{tokenId} | Get API keys |
| [**listApiTokens**](TokensApi.md#listApiTokens) | **GET** /orgs/{orgId}/api-tokens | List API keys |
| [**listApiTokensWithHttpInfo**](TokensApi.md#listApiTokensWithHttpInfo) | **GET** /orgs/{orgId}/api-tokens | List API keys |
| [**revokeApiToken**](TokensApi.md#revokeApiToken) | **DELETE** /orgs/{orgId}/api-tokens/{tokenId} | Revoke API keys |
| [**revokeApiTokenWithHttpInfo**](TokensApi.md#revokeApiTokenWithHttpInfo) | **DELETE** /orgs/{orgId}/api-tokens/{tokenId} | Revoke API keys |
| [**updateApiToken**](TokensApi.md#updateApiToken) | **PATCH** /orgs/{orgId}/api-tokens/{tokenId} | Update API keys |
| [**updateApiTokenWithHttpInfo**](TokensApi.md#updateApiTokenWithHttpInfo) | **PATCH** /orgs/{orgId}/api-tokens/{tokenId} | Update API keys |
| [**verifyApiToken**](TokensApi.md#verifyApiToken) | **POST** /api-tokens/verify | Verify API keys |
| [**verifyApiTokenWithHttpInfo**](TokensApi.md#verifyApiTokenWithHttpInfo) | **POST** /api-tokens/verify | Verify API keys |



## createApiToken

> CreateApiToken201Response createApiToken(createApiTokenRequest)

Create API keys

Creates a new API token for the specified organization. The full token is only shown once.

### Example

```java
// Import classes:
import com.zippendo.sdk.ApiClient;
import com.zippendo.sdk.ApiException;
import com.zippendo.sdk.Configuration;
import com.zippendo.sdk.auth.*;
import com.zippendo.sdk.models.*;
import com.zippendo.sdk.api.TokensApi;
import com.zippendo.sdk.api.TokensApi.*;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.zippendo.com");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        TokensApi apiInstance = new TokensApi(defaultClient);
        String orgId = "org_4d8af01qw2"; // String | Organization ID
        CreateApiTokenRequest createApiTokenRequest = new CreateApiTokenRequest(); // CreateApiTokenRequest | 
        try {
            APIcreateApiTokenRequest request = APIcreateApiTokenRequest.newBuilder()
                .orgId(orgId)
                .createApiTokenRequest(createApiTokenRequest)
                .build();
            CreateApiToken201Response result = apiInstance.createApiToken(request);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling TokensApi#createApiToken");
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
| createApiTokenRequest | [**APIcreateApiTokenRequest**](TokensApi.md#APIcreateApiTokenRequest)|-|-|

### Return type

[**CreateApiToken201Response**](CreateApiToken201Response.md)


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

## createApiTokenWithHttpInfo

> ApiResponse<CreateApiToken201Response> createApiTokenWithHttpInfo(createApiTokenRequest)

Create API keys

Creates a new API token for the specified organization. The full token is only shown once.

### Example

```java
// Import classes:
import com.zippendo.sdk.ApiClient;
import com.zippendo.sdk.ApiException;
import com.zippendo.sdk.ApiResponse;
import com.zippendo.sdk.Configuration;
import com.zippendo.sdk.auth.*;
import com.zippendo.sdk.models.*;
import com.zippendo.sdk.api.TokensApi;
import com.zippendo.sdk.api.TokensApi.*;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.zippendo.com");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        TokensApi apiInstance = new TokensApi(defaultClient);
        String orgId = "org_4d8af01qw2"; // String | Organization ID
        CreateApiTokenRequest createApiTokenRequest = new CreateApiTokenRequest(); // CreateApiTokenRequest | 
        try {
            APIcreateApiTokenRequest request = APIcreateApiTokenRequest.newBuilder()
                .orgId(orgId)
                .createApiTokenRequest(createApiTokenRequest)
                .build();
            ApiResponse<CreateApiToken201Response> response = apiInstance.createApiTokenWithHttpInfo(request);
            System.out.println("Status code: " + response.getStatusCode());
            System.out.println("Response headers: " + response.getHeaders());
            System.out.println("Response body: " + response.getData());
        } catch (ApiException e) {
            System.err.println("Exception when calling TokensApi#createApiToken");
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
| createApiTokenRequest | [**APIcreateApiTokenRequest**](TokensApi.md#APIcreateApiTokenRequest)|-|-|

### Return type

ApiResponse<[**CreateApiToken201Response**](CreateApiToken201Response.md)>


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


<a id="APIcreateApiTokenRequest"></a>
## APIcreateApiTokenRequest
### Properties

|     Name      |    Type       | Description   |     Notes    |
| ------------- | ------------- | ------------- | -------------|
| **orgId** | **String** | Organization ID | |
| **createApiTokenRequest** | [**CreateApiTokenRequest**](CreateApiTokenRequest.md) |  | |



## getApiToken

> ListApiTokens200ResponseDataInner getApiToken(getApiTokenRequest)

Get API keys

Returns metadata for a specific API token. The token secret is never returned.

### Example

```java
// Import classes:
import com.zippendo.sdk.ApiClient;
import com.zippendo.sdk.ApiException;
import com.zippendo.sdk.Configuration;
import com.zippendo.sdk.auth.*;
import com.zippendo.sdk.models.*;
import com.zippendo.sdk.api.TokensApi;
import com.zippendo.sdk.api.TokensApi.*;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.zippendo.com");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        TokensApi apiInstance = new TokensApi(defaultClient);
        String orgId = "org_4d8af01qw2"; // String | Organization ID
        String tokenId = "tok_6e2fa83ij9"; // String | API Token ID
        try {
            APIgetApiTokenRequest request = APIgetApiTokenRequest.newBuilder()
                .orgId(orgId)
                .tokenId(tokenId)
                .build();
            ListApiTokens200ResponseDataInner result = apiInstance.getApiToken(request);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling TokensApi#getApiToken");
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
| getApiTokenRequest | [**APIgetApiTokenRequest**](TokensApi.md#APIgetApiTokenRequest)|-|-|

### Return type

[**ListApiTokens200ResponseDataInner**](ListApiTokens200ResponseDataInner.md)


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

## getApiTokenWithHttpInfo

> ApiResponse<ListApiTokens200ResponseDataInner> getApiTokenWithHttpInfo(getApiTokenRequest)

Get API keys

Returns metadata for a specific API token. The token secret is never returned.

### Example

```java
// Import classes:
import com.zippendo.sdk.ApiClient;
import com.zippendo.sdk.ApiException;
import com.zippendo.sdk.ApiResponse;
import com.zippendo.sdk.Configuration;
import com.zippendo.sdk.auth.*;
import com.zippendo.sdk.models.*;
import com.zippendo.sdk.api.TokensApi;
import com.zippendo.sdk.api.TokensApi.*;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.zippendo.com");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        TokensApi apiInstance = new TokensApi(defaultClient);
        String orgId = "org_4d8af01qw2"; // String | Organization ID
        String tokenId = "tok_6e2fa83ij9"; // String | API Token ID
        try {
            APIgetApiTokenRequest request = APIgetApiTokenRequest.newBuilder()
                .orgId(orgId)
                .tokenId(tokenId)
                .build();
            ApiResponse<ListApiTokens200ResponseDataInner> response = apiInstance.getApiTokenWithHttpInfo(request);
            System.out.println("Status code: " + response.getStatusCode());
            System.out.println("Response headers: " + response.getHeaders());
            System.out.println("Response body: " + response.getData());
        } catch (ApiException e) {
            System.err.println("Exception when calling TokensApi#getApiToken");
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
| getApiTokenRequest | [**APIgetApiTokenRequest**](TokensApi.md#APIgetApiTokenRequest)|-|-|

### Return type

ApiResponse<[**ListApiTokens200ResponseDataInner**](ListApiTokens200ResponseDataInner.md)>


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


<a id="APIgetApiTokenRequest"></a>
## APIgetApiTokenRequest
### Properties

|     Name      |    Type       | Description   |     Notes    |
| ------------- | ------------- | ------------- | -------------|
| **orgId** | **String** | Organization ID | |
| **tokenId** | **String** | API Token ID | |



## listApiTokens

> ListApiTokens200Response listApiTokens(listApiTokensRequest)

List API keys

Returns a paginated list of API tokens belonging to the specified organization.

### Example

```java
// Import classes:
import com.zippendo.sdk.ApiClient;
import com.zippendo.sdk.ApiException;
import com.zippendo.sdk.Configuration;
import com.zippendo.sdk.auth.*;
import com.zippendo.sdk.models.*;
import com.zippendo.sdk.api.TokensApi;
import com.zippendo.sdk.api.TokensApi.*;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.zippendo.com");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        TokensApi apiInstance = new TokensApi(defaultClient);
        String orgId = "org_4d8af01qw2"; // String | Organization ID
        Integer page = 1; // Integer | Page number (1-based)
        Integer limit = 20; // Integer | Items per page (max 100)
        try {
            APIlistApiTokensRequest request = APIlistApiTokensRequest.newBuilder()
                .orgId(orgId)
                .page(page)
                .limit(limit)
                .build();
            ListApiTokens200Response result = apiInstance.listApiTokens(request);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling TokensApi#listApiTokens");
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
| listApiTokensRequest | [**APIlistApiTokensRequest**](TokensApi.md#APIlistApiTokensRequest)|-|-|

### Return type

[**ListApiTokens200Response**](ListApiTokens200Response.md)


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

## listApiTokensWithHttpInfo

> ApiResponse<ListApiTokens200Response> listApiTokensWithHttpInfo(listApiTokensRequest)

List API keys

Returns a paginated list of API tokens belonging to the specified organization.

### Example

```java
// Import classes:
import com.zippendo.sdk.ApiClient;
import com.zippendo.sdk.ApiException;
import com.zippendo.sdk.ApiResponse;
import com.zippendo.sdk.Configuration;
import com.zippendo.sdk.auth.*;
import com.zippendo.sdk.models.*;
import com.zippendo.sdk.api.TokensApi;
import com.zippendo.sdk.api.TokensApi.*;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.zippendo.com");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        TokensApi apiInstance = new TokensApi(defaultClient);
        String orgId = "org_4d8af01qw2"; // String | Organization ID
        Integer page = 1; // Integer | Page number (1-based)
        Integer limit = 20; // Integer | Items per page (max 100)
        try {
            APIlistApiTokensRequest request = APIlistApiTokensRequest.newBuilder()
                .orgId(orgId)
                .page(page)
                .limit(limit)
                .build();
            ApiResponse<ListApiTokens200Response> response = apiInstance.listApiTokensWithHttpInfo(request);
            System.out.println("Status code: " + response.getStatusCode());
            System.out.println("Response headers: " + response.getHeaders());
            System.out.println("Response body: " + response.getData());
        } catch (ApiException e) {
            System.err.println("Exception when calling TokensApi#listApiTokens");
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
| listApiTokensRequest | [**APIlistApiTokensRequest**](TokensApi.md#APIlistApiTokensRequest)|-|-|

### Return type

ApiResponse<[**ListApiTokens200Response**](ListApiTokens200Response.md)>


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


<a id="APIlistApiTokensRequest"></a>
## APIlistApiTokensRequest
### Properties

|     Name      |    Type       | Description   |     Notes    |
| ------------- | ------------- | ------------- | -------------|
| **orgId** | **String** | Organization ID | |
| **page** | **Integer** | Page number (1-based) | [optional] [default to 1] |
| **limit** | **Integer** | Items per page (max 100) | [optional] [default to 20] |



## revokeApiToken

> RevokeApiToken200Response revokeApiToken(revokeApiTokenRequest)

Revoke API keys

Revokes and deletes an API token.

### Example

```java
// Import classes:
import com.zippendo.sdk.ApiClient;
import com.zippendo.sdk.ApiException;
import com.zippendo.sdk.Configuration;
import com.zippendo.sdk.auth.*;
import com.zippendo.sdk.models.*;
import com.zippendo.sdk.api.TokensApi;
import com.zippendo.sdk.api.TokensApi.*;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.zippendo.com");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        TokensApi apiInstance = new TokensApi(defaultClient);
        String orgId = "org_4d8af01qw2"; // String | Organization ID
        String tokenId = "tok_6e2fa83ij9"; // String | API Token ID
        try {
            APIrevokeApiTokenRequest request = APIrevokeApiTokenRequest.newBuilder()
                .orgId(orgId)
                .tokenId(tokenId)
                .build();
            RevokeApiToken200Response result = apiInstance.revokeApiToken(request);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling TokensApi#revokeApiToken");
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
| revokeApiTokenRequest | [**APIrevokeApiTokenRequest**](TokensApi.md#APIrevokeApiTokenRequest)|-|-|

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
| **401** | Default Response |  -  |
| **403** | Default Response |  -  |
| **404** | Default Response |  -  |

## revokeApiTokenWithHttpInfo

> ApiResponse<RevokeApiToken200Response> revokeApiTokenWithHttpInfo(revokeApiTokenRequest)

Revoke API keys

Revokes and deletes an API token.

### Example

```java
// Import classes:
import com.zippendo.sdk.ApiClient;
import com.zippendo.sdk.ApiException;
import com.zippendo.sdk.ApiResponse;
import com.zippendo.sdk.Configuration;
import com.zippendo.sdk.auth.*;
import com.zippendo.sdk.models.*;
import com.zippendo.sdk.api.TokensApi;
import com.zippendo.sdk.api.TokensApi.*;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.zippendo.com");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        TokensApi apiInstance = new TokensApi(defaultClient);
        String orgId = "org_4d8af01qw2"; // String | Organization ID
        String tokenId = "tok_6e2fa83ij9"; // String | API Token ID
        try {
            APIrevokeApiTokenRequest request = APIrevokeApiTokenRequest.newBuilder()
                .orgId(orgId)
                .tokenId(tokenId)
                .build();
            ApiResponse<RevokeApiToken200Response> response = apiInstance.revokeApiTokenWithHttpInfo(request);
            System.out.println("Status code: " + response.getStatusCode());
            System.out.println("Response headers: " + response.getHeaders());
            System.out.println("Response body: " + response.getData());
        } catch (ApiException e) {
            System.err.println("Exception when calling TokensApi#revokeApiToken");
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
| revokeApiTokenRequest | [**APIrevokeApiTokenRequest**](TokensApi.md#APIrevokeApiTokenRequest)|-|-|

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
| **401** | Default Response |  -  |
| **403** | Default Response |  -  |
| **404** | Default Response |  -  |


<a id="APIrevokeApiTokenRequest"></a>
## APIrevokeApiTokenRequest
### Properties

|     Name      |    Type       | Description   |     Notes    |
| ------------- | ------------- | ------------- | -------------|
| **orgId** | **String** | Organization ID | |
| **tokenId** | **String** | API Token ID | |



## updateApiToken

> ListApiTokens200ResponseDataInner updateApiToken(updateApiTokenRequest)

Update API keys

Updates the name of an API token.

### Example

```java
// Import classes:
import com.zippendo.sdk.ApiClient;
import com.zippendo.sdk.ApiException;
import com.zippendo.sdk.Configuration;
import com.zippendo.sdk.auth.*;
import com.zippendo.sdk.models.*;
import com.zippendo.sdk.api.TokensApi;
import com.zippendo.sdk.api.TokensApi.*;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.zippendo.com");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        TokensApi apiInstance = new TokensApi(defaultClient);
        String orgId = "org_4d8af01qw2"; // String | Organization ID
        String tokenId = "tok_6e2fa83ij9"; // String | API Token ID
        UpdateApiTokenRequest updateApiTokenRequest = new UpdateApiTokenRequest(); // UpdateApiTokenRequest | 
        try {
            APIupdateApiTokenRequest request = APIupdateApiTokenRequest.newBuilder()
                .orgId(orgId)
                .tokenId(tokenId)
                .updateApiTokenRequest(updateApiTokenRequest)
                .build();
            ListApiTokens200ResponseDataInner result = apiInstance.updateApiToken(request);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling TokensApi#updateApiToken");
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
| updateApiTokenRequest | [**APIupdateApiTokenRequest**](TokensApi.md#APIupdateApiTokenRequest)|-|-|

### Return type

[**ListApiTokens200ResponseDataInner**](ListApiTokens200ResponseDataInner.md)


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

## updateApiTokenWithHttpInfo

> ApiResponse<ListApiTokens200ResponseDataInner> updateApiTokenWithHttpInfo(updateApiTokenRequest)

Update API keys

Updates the name of an API token.

### Example

```java
// Import classes:
import com.zippendo.sdk.ApiClient;
import com.zippendo.sdk.ApiException;
import com.zippendo.sdk.ApiResponse;
import com.zippendo.sdk.Configuration;
import com.zippendo.sdk.auth.*;
import com.zippendo.sdk.models.*;
import com.zippendo.sdk.api.TokensApi;
import com.zippendo.sdk.api.TokensApi.*;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.zippendo.com");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        TokensApi apiInstance = new TokensApi(defaultClient);
        String orgId = "org_4d8af01qw2"; // String | Organization ID
        String tokenId = "tok_6e2fa83ij9"; // String | API Token ID
        UpdateApiTokenRequest updateApiTokenRequest = new UpdateApiTokenRequest(); // UpdateApiTokenRequest | 
        try {
            APIupdateApiTokenRequest request = APIupdateApiTokenRequest.newBuilder()
                .orgId(orgId)
                .tokenId(tokenId)
                .updateApiTokenRequest(updateApiTokenRequest)
                .build();
            ApiResponse<ListApiTokens200ResponseDataInner> response = apiInstance.updateApiTokenWithHttpInfo(request);
            System.out.println("Status code: " + response.getStatusCode());
            System.out.println("Response headers: " + response.getHeaders());
            System.out.println("Response body: " + response.getData());
        } catch (ApiException e) {
            System.err.println("Exception when calling TokensApi#updateApiToken");
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
| updateApiTokenRequest | [**APIupdateApiTokenRequest**](TokensApi.md#APIupdateApiTokenRequest)|-|-|

### Return type

ApiResponse<[**ListApiTokens200ResponseDataInner**](ListApiTokens200ResponseDataInner.md)>


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


<a id="APIupdateApiTokenRequest"></a>
## APIupdateApiTokenRequest
### Properties

|     Name      |    Type       | Description   |     Notes    |
| ------------- | ------------- | ------------- | -------------|
| **orgId** | **String** | Organization ID | |
| **tokenId** | **String** | API Token ID | |
| **updateApiTokenRequest** | [**UpdateApiTokenRequest**](UpdateApiTokenRequest.md) |  | |



## verifyApiToken

> VerifyApiToken200Response verifyApiToken(verifyApiTokenRequest)

Verify API keys

Verifies whether an API token is valid and returns its metadata.

### Example

```java
// Import classes:
import com.zippendo.sdk.ApiClient;
import com.zippendo.sdk.ApiException;
import com.zippendo.sdk.Configuration;
import com.zippendo.sdk.auth.*;
import com.zippendo.sdk.models.*;
import com.zippendo.sdk.api.TokensApi;
import com.zippendo.sdk.api.TokensApi.*;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.zippendo.com");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        TokensApi apiInstance = new TokensApi(defaultClient);
        VerifyApiTokenRequest verifyApiTokenRequest = new VerifyApiTokenRequest(); // VerifyApiTokenRequest | 
        try {
            APIverifyApiTokenRequest request = APIverifyApiTokenRequest.newBuilder()
                .verifyApiTokenRequest(verifyApiTokenRequest)
                .build();
            VerifyApiToken200Response result = apiInstance.verifyApiToken(request);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling TokensApi#verifyApiToken");
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
| verifyApiTokenRequest | [**APIverifyApiTokenRequest**](TokensApi.md#APIverifyApiTokenRequest)|-|-|

### Return type

[**VerifyApiToken200Response**](VerifyApiToken200Response.md)


### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Default Response |  -  |

## verifyApiTokenWithHttpInfo

> ApiResponse<VerifyApiToken200Response> verifyApiTokenWithHttpInfo(verifyApiTokenRequest)

Verify API keys

Verifies whether an API token is valid and returns its metadata.

### Example

```java
// Import classes:
import com.zippendo.sdk.ApiClient;
import com.zippendo.sdk.ApiException;
import com.zippendo.sdk.ApiResponse;
import com.zippendo.sdk.Configuration;
import com.zippendo.sdk.auth.*;
import com.zippendo.sdk.models.*;
import com.zippendo.sdk.api.TokensApi;
import com.zippendo.sdk.api.TokensApi.*;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.zippendo.com");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        TokensApi apiInstance = new TokensApi(defaultClient);
        VerifyApiTokenRequest verifyApiTokenRequest = new VerifyApiTokenRequest(); // VerifyApiTokenRequest | 
        try {
            APIverifyApiTokenRequest request = APIverifyApiTokenRequest.newBuilder()
                .verifyApiTokenRequest(verifyApiTokenRequest)
                .build();
            ApiResponse<VerifyApiToken200Response> response = apiInstance.verifyApiTokenWithHttpInfo(request);
            System.out.println("Status code: " + response.getStatusCode());
            System.out.println("Response headers: " + response.getHeaders());
            System.out.println("Response body: " + response.getData());
        } catch (ApiException e) {
            System.err.println("Exception when calling TokensApi#verifyApiToken");
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
| verifyApiTokenRequest | [**APIverifyApiTokenRequest**](TokensApi.md#APIverifyApiTokenRequest)|-|-|

### Return type

ApiResponse<[**VerifyApiToken200Response**](VerifyApiToken200Response.md)>


### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Default Response |  -  |


<a id="APIverifyApiTokenRequest"></a>
## APIverifyApiTokenRequest
### Properties

|     Name      |    Type       | Description   |     Notes    |
| ------------- | ------------- | ------------- | -------------|
| **verifyApiTokenRequest** | [**VerifyApiTokenRequest**](VerifyApiTokenRequest.md) |  | |


