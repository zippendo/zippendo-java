# OrgsApi

All URIs are relative to *https://api.zippendo.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**deleteOrgLogo**](OrgsApi.md#deleteOrgLogo) | **DELETE** /orgs/{orgId}/branding/logo | Delete org logo |
| [**deleteOrgLogoWithHttpInfo**](OrgsApi.md#deleteOrgLogoWithHttpInfo) | **DELETE** /orgs/{orgId}/branding/logo | Delete org logo |
| [**getOrg**](OrgsApi.md#getOrg) | **GET** /orgs/{id} | Get org |
| [**getOrgWithHttpInfo**](OrgsApi.md#getOrgWithHttpInfo) | **GET** /orgs/{id} | Get org |
| [**getOrgBranding**](OrgsApi.md#getOrgBranding) | **GET** /orgs/{orgId}/branding | Get org branding |
| [**getOrgBrandingWithHttpInfo**](OrgsApi.md#getOrgBrandingWithHttpInfo) | **GET** /orgs/{orgId}/branding | Get org branding |
| [**getOrgLogo**](OrgsApi.md#getOrgLogo) | **GET** /orgs/{orgId}/branding/logo | Download org logo |
| [**getOrgLogoWithHttpInfo**](OrgsApi.md#getOrgLogoWithHttpInfo) | **GET** /orgs/{orgId}/branding/logo | Download org logo |
| [**updateOrg**](OrgsApi.md#updateOrg) | **PUT** /orgs/{id} | Update org |
| [**updateOrgWithHttpInfo**](OrgsApi.md#updateOrgWithHttpInfo) | **PUT** /orgs/{id} | Update org |
| [**updateOrgBranding**](OrgsApi.md#updateOrgBranding) | **PUT** /orgs/{orgId}/branding | Update org branding |
| [**updateOrgBrandingWithHttpInfo**](OrgsApi.md#updateOrgBrandingWithHttpInfo) | **PUT** /orgs/{orgId}/branding | Update org branding |
| [**uploadOrgLogo**](OrgsApi.md#uploadOrgLogo) | **POST** /orgs/{orgId}/branding/logo | Upload org logo |
| [**uploadOrgLogoWithHttpInfo**](OrgsApi.md#uploadOrgLogoWithHttpInfo) | **POST** /orgs/{orgId}/branding/logo | Upload org logo |



## deleteOrgLogo

> GetOrgBranding200Response deleteOrgLogo(deleteOrgLogoRequest)

Delete org logo

Removes the org logo. Requires the customBranding entitlement.

### Example

```java
// Import classes:
import com.zippendo.sdk.ApiClient;
import com.zippendo.sdk.ApiException;
import com.zippendo.sdk.Configuration;
import com.zippendo.sdk.auth.*;
import com.zippendo.sdk.models.*;
import com.zippendo.sdk.api.OrgsApi;
import com.zippendo.sdk.api.OrgsApi.*;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.zippendo.com");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        OrgsApi apiInstance = new OrgsApi(defaultClient);
        String orgId = "org_8f3kd92ld0"; // String | Organization ID
        try {
            APIdeleteOrgLogoRequest request = APIdeleteOrgLogoRequest.newBuilder()
                .orgId(orgId)
                .build();
            GetOrgBranding200Response result = apiInstance.deleteOrgLogo(request);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling OrgsApi#deleteOrgLogo");
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
| deleteOrgLogoRequest | [**APIdeleteOrgLogoRequest**](OrgsApi.md#APIdeleteOrgLogoRequest)|-|-|

### Return type

[**GetOrgBranding200Response**](GetOrgBranding200Response.md)


### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Default Response |  -  |
| **404** | Default Response |  -  |

## deleteOrgLogoWithHttpInfo

> ApiResponse<GetOrgBranding200Response> deleteOrgLogoWithHttpInfo(deleteOrgLogoRequest)

Delete org logo

Removes the org logo. Requires the customBranding entitlement.

### Example

```java
// Import classes:
import com.zippendo.sdk.ApiClient;
import com.zippendo.sdk.ApiException;
import com.zippendo.sdk.ApiResponse;
import com.zippendo.sdk.Configuration;
import com.zippendo.sdk.auth.*;
import com.zippendo.sdk.models.*;
import com.zippendo.sdk.api.OrgsApi;
import com.zippendo.sdk.api.OrgsApi.*;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.zippendo.com");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        OrgsApi apiInstance = new OrgsApi(defaultClient);
        String orgId = "org_8f3kd92ld0"; // String | Organization ID
        try {
            APIdeleteOrgLogoRequest request = APIdeleteOrgLogoRequest.newBuilder()
                .orgId(orgId)
                .build();
            ApiResponse<GetOrgBranding200Response> response = apiInstance.deleteOrgLogoWithHttpInfo(request);
            System.out.println("Status code: " + response.getStatusCode());
            System.out.println("Response headers: " + response.getHeaders());
            System.out.println("Response body: " + response.getData());
        } catch (ApiException e) {
            System.err.println("Exception when calling OrgsApi#deleteOrgLogo");
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
| deleteOrgLogoRequest | [**APIdeleteOrgLogoRequest**](OrgsApi.md#APIdeleteOrgLogoRequest)|-|-|

### Return type

ApiResponse<[**GetOrgBranding200Response**](GetOrgBranding200Response.md)>


### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Default Response |  -  |
| **404** | Default Response |  -  |


<a id="APIdeleteOrgLogoRequest"></a>
## APIdeleteOrgLogoRequest
### Properties

|     Name      |    Type       | Description   |     Notes    |
| ------------- | ------------- | ------------- | -------------|
| **orgId** | **String** | Organization ID | |



## getOrg

> GetOrg200Response getOrg(getOrgRequest)

Get org

Returns a specific organization by ID, including its member count.

### Example

```java
// Import classes:
import com.zippendo.sdk.ApiClient;
import com.zippendo.sdk.ApiException;
import com.zippendo.sdk.Configuration;
import com.zippendo.sdk.auth.*;
import com.zippendo.sdk.models.*;
import com.zippendo.sdk.api.OrgsApi;
import com.zippendo.sdk.api.OrgsApi.*;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.zippendo.com");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        OrgsApi apiInstance = new OrgsApi(defaultClient);
        String id = "clz9x8a7b0001"; // String | Resource ID
        try {
            APIgetOrgRequest request = APIgetOrgRequest.newBuilder()
                .id(id)
                .build();
            GetOrg200Response result = apiInstance.getOrg(request);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling OrgsApi#getOrg");
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
| getOrgRequest | [**APIgetOrgRequest**](OrgsApi.md#APIgetOrgRequest)|-|-|

### Return type

[**GetOrg200Response**](GetOrg200Response.md)


### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Default Response |  -  |
| **404** | Default Response |  -  |

## getOrgWithHttpInfo

> ApiResponse<GetOrg200Response> getOrgWithHttpInfo(getOrgRequest)

Get org

Returns a specific organization by ID, including its member count.

### Example

```java
// Import classes:
import com.zippendo.sdk.ApiClient;
import com.zippendo.sdk.ApiException;
import com.zippendo.sdk.ApiResponse;
import com.zippendo.sdk.Configuration;
import com.zippendo.sdk.auth.*;
import com.zippendo.sdk.models.*;
import com.zippendo.sdk.api.OrgsApi;
import com.zippendo.sdk.api.OrgsApi.*;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.zippendo.com");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        OrgsApi apiInstance = new OrgsApi(defaultClient);
        String id = "clz9x8a7b0001"; // String | Resource ID
        try {
            APIgetOrgRequest request = APIgetOrgRequest.newBuilder()
                .id(id)
                .build();
            ApiResponse<GetOrg200Response> response = apiInstance.getOrgWithHttpInfo(request);
            System.out.println("Status code: " + response.getStatusCode());
            System.out.println("Response headers: " + response.getHeaders());
            System.out.println("Response body: " + response.getData());
        } catch (ApiException e) {
            System.err.println("Exception when calling OrgsApi#getOrg");
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
| getOrgRequest | [**APIgetOrgRequest**](OrgsApi.md#APIgetOrgRequest)|-|-|

### Return type

ApiResponse<[**GetOrg200Response**](GetOrg200Response.md)>


### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Default Response |  -  |
| **404** | Default Response |  -  |


<a id="APIgetOrgRequest"></a>
## APIgetOrgRequest
### Properties

|     Name      |    Type       | Description   |     Notes    |
| ------------- | ------------- | ------------- | -------------|
| **id** | **String** | Resource ID | |



## getOrgBranding

> GetOrgBranding200Response getOrgBranding(getOrgBrandingRequest)

Get org branding

Returns the org&#39;s brand colors and an authenticated URL to download the logo.

### Example

```java
// Import classes:
import com.zippendo.sdk.ApiClient;
import com.zippendo.sdk.ApiException;
import com.zippendo.sdk.Configuration;
import com.zippendo.sdk.auth.*;
import com.zippendo.sdk.models.*;
import com.zippendo.sdk.api.OrgsApi;
import com.zippendo.sdk.api.OrgsApi.*;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.zippendo.com");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        OrgsApi apiInstance = new OrgsApi(defaultClient);
        String orgId = "org_8f3kd92ld0"; // String | Organization ID
        try {
            APIgetOrgBrandingRequest request = APIgetOrgBrandingRequest.newBuilder()
                .orgId(orgId)
                .build();
            GetOrgBranding200Response result = apiInstance.getOrgBranding(request);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling OrgsApi#getOrgBranding");
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
| getOrgBrandingRequest | [**APIgetOrgBrandingRequest**](OrgsApi.md#APIgetOrgBrandingRequest)|-|-|

### Return type

[**GetOrgBranding200Response**](GetOrgBranding200Response.md)


### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Default Response |  -  |
| **404** | Default Response |  -  |

## getOrgBrandingWithHttpInfo

> ApiResponse<GetOrgBranding200Response> getOrgBrandingWithHttpInfo(getOrgBrandingRequest)

Get org branding

Returns the org&#39;s brand colors and an authenticated URL to download the logo.

### Example

```java
// Import classes:
import com.zippendo.sdk.ApiClient;
import com.zippendo.sdk.ApiException;
import com.zippendo.sdk.ApiResponse;
import com.zippendo.sdk.Configuration;
import com.zippendo.sdk.auth.*;
import com.zippendo.sdk.models.*;
import com.zippendo.sdk.api.OrgsApi;
import com.zippendo.sdk.api.OrgsApi.*;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.zippendo.com");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        OrgsApi apiInstance = new OrgsApi(defaultClient);
        String orgId = "org_8f3kd92ld0"; // String | Organization ID
        try {
            APIgetOrgBrandingRequest request = APIgetOrgBrandingRequest.newBuilder()
                .orgId(orgId)
                .build();
            ApiResponse<GetOrgBranding200Response> response = apiInstance.getOrgBrandingWithHttpInfo(request);
            System.out.println("Status code: " + response.getStatusCode());
            System.out.println("Response headers: " + response.getHeaders());
            System.out.println("Response body: " + response.getData());
        } catch (ApiException e) {
            System.err.println("Exception when calling OrgsApi#getOrgBranding");
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
| getOrgBrandingRequest | [**APIgetOrgBrandingRequest**](OrgsApi.md#APIgetOrgBrandingRequest)|-|-|

### Return type

ApiResponse<[**GetOrgBranding200Response**](GetOrgBranding200Response.md)>


### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Default Response |  -  |
| **404** | Default Response |  -  |


<a id="APIgetOrgBrandingRequest"></a>
## APIgetOrgBrandingRequest
### Properties

|     Name      |    Type       | Description   |     Notes    |
| ------------- | ------------- | ------------- | -------------|
| **orgId** | **String** | Organization ID | |



## getOrgLogo

> File getOrgLogo(getOrgLogoRequest)

Download org logo

Returns the org logo image bytes with the stored content type.

### Example

```java
// Import classes:
import com.zippendo.sdk.ApiClient;
import com.zippendo.sdk.ApiException;
import com.zippendo.sdk.Configuration;
import com.zippendo.sdk.auth.*;
import com.zippendo.sdk.models.*;
import com.zippendo.sdk.api.OrgsApi;
import com.zippendo.sdk.api.OrgsApi.*;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.zippendo.com");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        OrgsApi apiInstance = new OrgsApi(defaultClient);
        String orgId = "org_8f3kd92ld0"; // String | Organization ID
        try {
            APIgetOrgLogoRequest request = APIgetOrgLogoRequest.newBuilder()
                .orgId(orgId)
                .build();
            File result = apiInstance.getOrgLogo(request);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling OrgsApi#getOrgLogo");
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
| getOrgLogoRequest | [**APIgetOrgLogoRequest**](OrgsApi.md#APIgetOrgLogoRequest)|-|-|

### Return type

[**File**](File.md)


### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: image/png, image/jpeg, image/webp

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The logo image bytes |  -  |
| **404** | Default Response |  -  |

## getOrgLogoWithHttpInfo

> ApiResponse<File> getOrgLogoWithHttpInfo(getOrgLogoRequest)

Download org logo

Returns the org logo image bytes with the stored content type.

### Example

```java
// Import classes:
import com.zippendo.sdk.ApiClient;
import com.zippendo.sdk.ApiException;
import com.zippendo.sdk.ApiResponse;
import com.zippendo.sdk.Configuration;
import com.zippendo.sdk.auth.*;
import com.zippendo.sdk.models.*;
import com.zippendo.sdk.api.OrgsApi;
import com.zippendo.sdk.api.OrgsApi.*;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.zippendo.com");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        OrgsApi apiInstance = new OrgsApi(defaultClient);
        String orgId = "org_8f3kd92ld0"; // String | Organization ID
        try {
            APIgetOrgLogoRequest request = APIgetOrgLogoRequest.newBuilder()
                .orgId(orgId)
                .build();
            ApiResponse<File> response = apiInstance.getOrgLogoWithHttpInfo(request);
            System.out.println("Status code: " + response.getStatusCode());
            System.out.println("Response headers: " + response.getHeaders());
            System.out.println("Response body: " + response.getData());
        } catch (ApiException e) {
            System.err.println("Exception when calling OrgsApi#getOrgLogo");
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
| getOrgLogoRequest | [**APIgetOrgLogoRequest**](OrgsApi.md#APIgetOrgLogoRequest)|-|-|

### Return type

ApiResponse<[**File**](File.md)>


### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: image/png, image/jpeg, image/webp

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The logo image bytes |  -  |
| **404** | Default Response |  -  |


<a id="APIgetOrgLogoRequest"></a>
## APIgetOrgLogoRequest
### Properties

|     Name      |    Type       | Description   |     Notes    |
| ------------- | ------------- | ------------- | -------------|
| **orgId** | **String** | Organization ID | |



## updateOrg

> UpdateOrg200Response updateOrg(updateOrgRequest)

Update org

Updates an existing organization&#39;s profile, billing, and customs settings.

### Example

```java
// Import classes:
import com.zippendo.sdk.ApiClient;
import com.zippendo.sdk.ApiException;
import com.zippendo.sdk.Configuration;
import com.zippendo.sdk.auth.*;
import com.zippendo.sdk.models.*;
import com.zippendo.sdk.api.OrgsApi;
import com.zippendo.sdk.api.OrgsApi.*;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.zippendo.com");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        OrgsApi apiInstance = new OrgsApi(defaultClient);
        String id = "clz9x8a7b0001"; // String | Resource ID
        UpdateOrgRequest updateOrgRequest = new UpdateOrgRequest(); // UpdateOrgRequest | 
        try {
            APIupdateOrgRequest request = APIupdateOrgRequest.newBuilder()
                .id(id)
                .updateOrgRequest(updateOrgRequest)
                .build();
            UpdateOrg200Response result = apiInstance.updateOrg(request);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling OrgsApi#updateOrg");
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
| updateOrgRequest | [**APIupdateOrgRequest**](OrgsApi.md#APIupdateOrgRequest)|-|-|

### Return type

[**UpdateOrg200Response**](UpdateOrg200Response.md)


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

## updateOrgWithHttpInfo

> ApiResponse<UpdateOrg200Response> updateOrgWithHttpInfo(updateOrgRequest)

Update org

Updates an existing organization&#39;s profile, billing, and customs settings.

### Example

```java
// Import classes:
import com.zippendo.sdk.ApiClient;
import com.zippendo.sdk.ApiException;
import com.zippendo.sdk.ApiResponse;
import com.zippendo.sdk.Configuration;
import com.zippendo.sdk.auth.*;
import com.zippendo.sdk.models.*;
import com.zippendo.sdk.api.OrgsApi;
import com.zippendo.sdk.api.OrgsApi.*;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.zippendo.com");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        OrgsApi apiInstance = new OrgsApi(defaultClient);
        String id = "clz9x8a7b0001"; // String | Resource ID
        UpdateOrgRequest updateOrgRequest = new UpdateOrgRequest(); // UpdateOrgRequest | 
        try {
            APIupdateOrgRequest request = APIupdateOrgRequest.newBuilder()
                .id(id)
                .updateOrgRequest(updateOrgRequest)
                .build();
            ApiResponse<UpdateOrg200Response> response = apiInstance.updateOrgWithHttpInfo(request);
            System.out.println("Status code: " + response.getStatusCode());
            System.out.println("Response headers: " + response.getHeaders());
            System.out.println("Response body: " + response.getData());
        } catch (ApiException e) {
            System.err.println("Exception when calling OrgsApi#updateOrg");
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
| updateOrgRequest | [**APIupdateOrgRequest**](OrgsApi.md#APIupdateOrgRequest)|-|-|

### Return type

ApiResponse<[**UpdateOrg200Response**](UpdateOrg200Response.md)>


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


<a id="APIupdateOrgRequest"></a>
## APIupdateOrgRequest
### Properties

|     Name      |    Type       | Description   |     Notes    |
| ------------- | ------------- | ------------- | -------------|
| **id** | **String** | Resource ID | |
| **updateOrgRequest** | [**UpdateOrgRequest**](UpdateOrgRequest.md) |  | |



## updateOrgBranding

> GetOrgBranding200Response updateOrgBranding(updateOrgBrandingRequest)

Update org branding

Sets the org brand colors. Requires the customBranding entitlement.

### Example

```java
// Import classes:
import com.zippendo.sdk.ApiClient;
import com.zippendo.sdk.ApiException;
import com.zippendo.sdk.Configuration;
import com.zippendo.sdk.auth.*;
import com.zippendo.sdk.models.*;
import com.zippendo.sdk.api.OrgsApi;
import com.zippendo.sdk.api.OrgsApi.*;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.zippendo.com");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        OrgsApi apiInstance = new OrgsApi(defaultClient);
        String orgId = "org_8f3kd92ld0"; // String | Organization ID
        UpdateOrgBrandingRequest updateOrgBrandingRequest = new UpdateOrgBrandingRequest(); // UpdateOrgBrandingRequest | 
        try {
            APIupdateOrgBrandingRequest request = APIupdateOrgBrandingRequest.newBuilder()
                .orgId(orgId)
                .updateOrgBrandingRequest(updateOrgBrandingRequest)
                .build();
            GetOrgBranding200Response result = apiInstance.updateOrgBranding(request);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling OrgsApi#updateOrgBranding");
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
| updateOrgBrandingRequest | [**APIupdateOrgBrandingRequest**](OrgsApi.md#APIupdateOrgBrandingRequest)|-|-|

### Return type

[**GetOrgBranding200Response**](GetOrgBranding200Response.md)


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

## updateOrgBrandingWithHttpInfo

> ApiResponse<GetOrgBranding200Response> updateOrgBrandingWithHttpInfo(updateOrgBrandingRequest)

Update org branding

Sets the org brand colors. Requires the customBranding entitlement.

### Example

```java
// Import classes:
import com.zippendo.sdk.ApiClient;
import com.zippendo.sdk.ApiException;
import com.zippendo.sdk.ApiResponse;
import com.zippendo.sdk.Configuration;
import com.zippendo.sdk.auth.*;
import com.zippendo.sdk.models.*;
import com.zippendo.sdk.api.OrgsApi;
import com.zippendo.sdk.api.OrgsApi.*;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.zippendo.com");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        OrgsApi apiInstance = new OrgsApi(defaultClient);
        String orgId = "org_8f3kd92ld0"; // String | Organization ID
        UpdateOrgBrandingRequest updateOrgBrandingRequest = new UpdateOrgBrandingRequest(); // UpdateOrgBrandingRequest | 
        try {
            APIupdateOrgBrandingRequest request = APIupdateOrgBrandingRequest.newBuilder()
                .orgId(orgId)
                .updateOrgBrandingRequest(updateOrgBrandingRequest)
                .build();
            ApiResponse<GetOrgBranding200Response> response = apiInstance.updateOrgBrandingWithHttpInfo(request);
            System.out.println("Status code: " + response.getStatusCode());
            System.out.println("Response headers: " + response.getHeaders());
            System.out.println("Response body: " + response.getData());
        } catch (ApiException e) {
            System.err.println("Exception when calling OrgsApi#updateOrgBranding");
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
| updateOrgBrandingRequest | [**APIupdateOrgBrandingRequest**](OrgsApi.md#APIupdateOrgBrandingRequest)|-|-|

### Return type

ApiResponse<[**GetOrgBranding200Response**](GetOrgBranding200Response.md)>


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


<a id="APIupdateOrgBrandingRequest"></a>
## APIupdateOrgBrandingRequest
### Properties

|     Name      |    Type       | Description   |     Notes    |
| ------------- | ------------- | ------------- | -------------|
| **orgId** | **String** | Organization ID | |
| **updateOrgBrandingRequest** | [**UpdateOrgBrandingRequest**](UpdateOrgBrandingRequest.md) |  | |



## uploadOrgLogo

> GetOrgBranding200Response uploadOrgLogo(uploadOrgLogoRequest)

Upload org logo

Uploads the org logo as multipart/form-data. Accepts PNG, JPG, or WEBP up to 5MB and 4096×4096px; the image is re-encoded and stored. Requires the customBranding entitlement.

### Example

```java
// Import classes:
import com.zippendo.sdk.ApiClient;
import com.zippendo.sdk.ApiException;
import com.zippendo.sdk.Configuration;
import com.zippendo.sdk.auth.*;
import com.zippendo.sdk.models.*;
import com.zippendo.sdk.api.OrgsApi;
import com.zippendo.sdk.api.OrgsApi.*;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.zippendo.com");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        OrgsApi apiInstance = new OrgsApi(defaultClient);
        String orgId = "org_8f3kd92ld0"; // String | Organization ID
        File _file = new File("/path/to/file"); // File | Image file (PNG, JPG, or WEBP)
        try {
            APIuploadOrgLogoRequest request = APIuploadOrgLogoRequest.newBuilder()
                .orgId(orgId)
                ._file(_file)
                .build();
            GetOrgBranding200Response result = apiInstance.uploadOrgLogo(request);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling OrgsApi#uploadOrgLogo");
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
| uploadOrgLogoRequest | [**APIuploadOrgLogoRequest**](OrgsApi.md#APIuploadOrgLogoRequest)|-|-|

### Return type

[**GetOrgBranding200Response**](GetOrgBranding200Response.md)


### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: multipart/form-data
- **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Default Response |  -  |
| **400** | Default Response |  -  |
| **403** | Default Response |  -  |
| **404** | Default Response |  -  |
| **413** | Default Response |  -  |

## uploadOrgLogoWithHttpInfo

> ApiResponse<GetOrgBranding200Response> uploadOrgLogoWithHttpInfo(uploadOrgLogoRequest)

Upload org logo

Uploads the org logo as multipart/form-data. Accepts PNG, JPG, or WEBP up to 5MB and 4096×4096px; the image is re-encoded and stored. Requires the customBranding entitlement.

### Example

```java
// Import classes:
import com.zippendo.sdk.ApiClient;
import com.zippendo.sdk.ApiException;
import com.zippendo.sdk.ApiResponse;
import com.zippendo.sdk.Configuration;
import com.zippendo.sdk.auth.*;
import com.zippendo.sdk.models.*;
import com.zippendo.sdk.api.OrgsApi;
import com.zippendo.sdk.api.OrgsApi.*;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.zippendo.com");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        OrgsApi apiInstance = new OrgsApi(defaultClient);
        String orgId = "org_8f3kd92ld0"; // String | Organization ID
        File _file = new File("/path/to/file"); // File | Image file (PNG, JPG, or WEBP)
        try {
            APIuploadOrgLogoRequest request = APIuploadOrgLogoRequest.newBuilder()
                .orgId(orgId)
                ._file(_file)
                .build();
            ApiResponse<GetOrgBranding200Response> response = apiInstance.uploadOrgLogoWithHttpInfo(request);
            System.out.println("Status code: " + response.getStatusCode());
            System.out.println("Response headers: " + response.getHeaders());
            System.out.println("Response body: " + response.getData());
        } catch (ApiException e) {
            System.err.println("Exception when calling OrgsApi#uploadOrgLogo");
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
| uploadOrgLogoRequest | [**APIuploadOrgLogoRequest**](OrgsApi.md#APIuploadOrgLogoRequest)|-|-|

### Return type

ApiResponse<[**GetOrgBranding200Response**](GetOrgBranding200Response.md)>


### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: multipart/form-data
- **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Default Response |  -  |
| **400** | Default Response |  -  |
| **403** | Default Response |  -  |
| **404** | Default Response |  -  |
| **413** | Default Response |  -  |


<a id="APIuploadOrgLogoRequest"></a>
## APIuploadOrgLogoRequest
### Properties

|     Name      |    Type       | Description   |     Notes    |
| ------------- | ------------- | ------------- | -------------|
| **orgId** | **String** | Organization ID | |
| **_file** | **File** | Image file (PNG, JPG, or WEBP) | |


