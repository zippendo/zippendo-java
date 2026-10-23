# BrandsApi

All URIs are relative to *https://api.zippendo.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**archiveOrgBrand**](BrandsApi.md#archiveOrgBrand) | **POST** /orgs/{orgId}/brands/{brandId}/archive | Archive brand |
| [**archiveOrgBrandWithHttpInfo**](BrandsApi.md#archiveOrgBrandWithHttpInfo) | **POST** /orgs/{orgId}/brands/{brandId}/archive | Archive brand |
| [**checkBrandSlug**](BrandsApi.md#checkBrandSlug) | **GET** /orgs/{orgId}/brands/check-slug/{slug} | Check brand slug availability |
| [**checkBrandSlugWithHttpInfo**](BrandsApi.md#checkBrandSlugWithHttpInfo) | **GET** /orgs/{orgId}/brands/check-slug/{slug} | Check brand slug availability |
| [**createOrgBrand**](BrandsApi.md#createOrgBrand) | **POST** /orgs/{orgId}/brands | Create brand |
| [**createOrgBrandWithHttpInfo**](BrandsApi.md#createOrgBrandWithHttpInfo) | **POST** /orgs/{orgId}/brands | Create brand |
| [**deleteBrandLogo**](BrandsApi.md#deleteBrandLogo) | **DELETE** /orgs/{orgId}/brands/{brandId}/logo | Delete brand logo |
| [**deleteBrandLogoWithHttpInfo**](BrandsApi.md#deleteBrandLogoWithHttpInfo) | **DELETE** /orgs/{orgId}/brands/{brandId}/logo | Delete brand logo |
| [**getBrandLogo**](BrandsApi.md#getBrandLogo) | **GET** /orgs/{orgId}/brands/{brandId}/logo | Get brand logo |
| [**getBrandLogoWithHttpInfo**](BrandsApi.md#getBrandLogoWithHttpInfo) | **GET** /orgs/{orgId}/brands/{brandId}/logo | Get brand logo |
| [**getOrgBrand**](BrandsApi.md#getOrgBrand) | **GET** /orgs/{orgId}/brands/{brandId} | Get brand |
| [**getOrgBrandWithHttpInfo**](BrandsApi.md#getOrgBrandWithHttpInfo) | **GET** /orgs/{orgId}/brands/{brandId} | Get brand |
| [**listOrgBrands**](BrandsApi.md#listOrgBrands) | **GET** /orgs/{orgId}/brands | List brands |
| [**listOrgBrandsWithHttpInfo**](BrandsApi.md#listOrgBrandsWithHttpInfo) | **GET** /orgs/{orgId}/brands | List brands |
| [**unarchiveOrgBrand**](BrandsApi.md#unarchiveOrgBrand) | **POST** /orgs/{orgId}/brands/{brandId}/unarchive | Unarchive brand |
| [**unarchiveOrgBrandWithHttpInfo**](BrandsApi.md#unarchiveOrgBrandWithHttpInfo) | **POST** /orgs/{orgId}/brands/{brandId}/unarchive | Unarchive brand |
| [**updateOrgBrand**](BrandsApi.md#updateOrgBrand) | **PATCH** /orgs/{orgId}/brands/{brandId} | Update brand |
| [**updateOrgBrandWithHttpInfo**](BrandsApi.md#updateOrgBrandWithHttpInfo) | **PATCH** /orgs/{orgId}/brands/{brandId} | Update brand |
| [**uploadBrandLogo**](BrandsApi.md#uploadBrandLogo) | **POST** /orgs/{orgId}/brands/{brandId}/logo | Upload brand logo |
| [**uploadBrandLogoWithHttpInfo**](BrandsApi.md#uploadBrandLogoWithHttpInfo) | **POST** /orgs/{orgId}/brands/{brandId}/logo | Upload brand logo |



## archiveOrgBrand

> ListOrgBrands200ResponseDataInner archiveOrgBrand(archiveOrgBrandRequest)

Archive brand

Archives a brand: it leaves the brand switcher and default listings, but its orders, shipments and settings are retained and remain visible in the organization-wide view.

### Example

```java
// Import classes:
import com.zippendo.sdk.ApiClient;
import com.zippendo.sdk.ApiException;
import com.zippendo.sdk.Configuration;
import com.zippendo.sdk.auth.*;
import com.zippendo.sdk.models.*;
import com.zippendo.sdk.api.BrandsApi;
import com.zippendo.sdk.api.BrandsApi.*;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.zippendo.com");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        BrandsApi apiInstance = new BrandsApi(defaultClient);
        String orgId = "org_8f3kd92ld0"; // String | Organization ID
        String brandId = "brnd_8f3kd92ld0"; // String | Brand ID
        try {
            APIarchiveOrgBrandRequest request = APIarchiveOrgBrandRequest.newBuilder()
                .orgId(orgId)
                .brandId(brandId)
                .build();
            ListOrgBrands200ResponseDataInner result = apiInstance.archiveOrgBrand(request);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling BrandsApi#archiveOrgBrand");
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
| archiveOrgBrandRequest | [**APIarchiveOrgBrandRequest**](BrandsApi.md#APIarchiveOrgBrandRequest)|-|-|

### Return type

[**ListOrgBrands200ResponseDataInner**](ListOrgBrands200ResponseDataInner.md)


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

## archiveOrgBrandWithHttpInfo

> ApiResponse<ListOrgBrands200ResponseDataInner> archiveOrgBrandWithHttpInfo(archiveOrgBrandRequest)

Archive brand

Archives a brand: it leaves the brand switcher and default listings, but its orders, shipments and settings are retained and remain visible in the organization-wide view.

### Example

```java
// Import classes:
import com.zippendo.sdk.ApiClient;
import com.zippendo.sdk.ApiException;
import com.zippendo.sdk.ApiResponse;
import com.zippendo.sdk.Configuration;
import com.zippendo.sdk.auth.*;
import com.zippendo.sdk.models.*;
import com.zippendo.sdk.api.BrandsApi;
import com.zippendo.sdk.api.BrandsApi.*;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.zippendo.com");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        BrandsApi apiInstance = new BrandsApi(defaultClient);
        String orgId = "org_8f3kd92ld0"; // String | Organization ID
        String brandId = "brnd_8f3kd92ld0"; // String | Brand ID
        try {
            APIarchiveOrgBrandRequest request = APIarchiveOrgBrandRequest.newBuilder()
                .orgId(orgId)
                .brandId(brandId)
                .build();
            ApiResponse<ListOrgBrands200ResponseDataInner> response = apiInstance.archiveOrgBrandWithHttpInfo(request);
            System.out.println("Status code: " + response.getStatusCode());
            System.out.println("Response headers: " + response.getHeaders());
            System.out.println("Response body: " + response.getData());
        } catch (ApiException e) {
            System.err.println("Exception when calling BrandsApi#archiveOrgBrand");
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
| archiveOrgBrandRequest | [**APIarchiveOrgBrandRequest**](BrandsApi.md#APIarchiveOrgBrandRequest)|-|-|

### Return type

ApiResponse<[**ListOrgBrands200ResponseDataInner**](ListOrgBrands200ResponseDataInner.md)>


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


<a id="APIarchiveOrgBrandRequest"></a>
## APIarchiveOrgBrandRequest
### Properties

|     Name      |    Type       | Description   |     Notes    |
| ------------- | ------------- | ------------- | -------------|
| **orgId** | **String** | Organization ID | |
| **brandId** | **String** | Brand ID | |



## checkBrandSlug

> CheckBrandSlug200Response checkBrandSlug(checkBrandSlugRequest)

Check brand slug availability

Reports whether a brand slug is free within this organization. Brand slugs are unique per organization, so the same slug may exist in another organization. Archived brands still hold their slug.

### Example

```java
// Import classes:
import com.zippendo.sdk.ApiClient;
import com.zippendo.sdk.ApiException;
import com.zippendo.sdk.Configuration;
import com.zippendo.sdk.auth.*;
import com.zippendo.sdk.models.*;
import com.zippendo.sdk.api.BrandsApi;
import com.zippendo.sdk.api.BrandsApi.*;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.zippendo.com");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        BrandsApi apiInstance = new BrandsApi(defaultClient);
        String orgId = "org_8f3kd92ld0"; // String | Organization ID
        String slug = "acme"; // String | Brand slug to check
        try {
            APIcheckBrandSlugRequest request = APIcheckBrandSlugRequest.newBuilder()
                .orgId(orgId)
                .slug(slug)
                .build();
            CheckBrandSlug200Response result = apiInstance.checkBrandSlug(request);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling BrandsApi#checkBrandSlug");
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
| checkBrandSlugRequest | [**APIcheckBrandSlugRequest**](BrandsApi.md#APIcheckBrandSlugRequest)|-|-|

### Return type

[**CheckBrandSlug200Response**](CheckBrandSlug200Response.md)


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
| **401** | Default Response |  -  |
| **403** | Default Response |  -  |

## checkBrandSlugWithHttpInfo

> ApiResponse<CheckBrandSlug200Response> checkBrandSlugWithHttpInfo(checkBrandSlugRequest)

Check brand slug availability

Reports whether a brand slug is free within this organization. Brand slugs are unique per organization, so the same slug may exist in another organization. Archived brands still hold their slug.

### Example

```java
// Import classes:
import com.zippendo.sdk.ApiClient;
import com.zippendo.sdk.ApiException;
import com.zippendo.sdk.ApiResponse;
import com.zippendo.sdk.Configuration;
import com.zippendo.sdk.auth.*;
import com.zippendo.sdk.models.*;
import com.zippendo.sdk.api.BrandsApi;
import com.zippendo.sdk.api.BrandsApi.*;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.zippendo.com");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        BrandsApi apiInstance = new BrandsApi(defaultClient);
        String orgId = "org_8f3kd92ld0"; // String | Organization ID
        String slug = "acme"; // String | Brand slug to check
        try {
            APIcheckBrandSlugRequest request = APIcheckBrandSlugRequest.newBuilder()
                .orgId(orgId)
                .slug(slug)
                .build();
            ApiResponse<CheckBrandSlug200Response> response = apiInstance.checkBrandSlugWithHttpInfo(request);
            System.out.println("Status code: " + response.getStatusCode());
            System.out.println("Response headers: " + response.getHeaders());
            System.out.println("Response body: " + response.getData());
        } catch (ApiException e) {
            System.err.println("Exception when calling BrandsApi#checkBrandSlug");
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
| checkBrandSlugRequest | [**APIcheckBrandSlugRequest**](BrandsApi.md#APIcheckBrandSlugRequest)|-|-|

### Return type

ApiResponse<[**CheckBrandSlug200Response**](CheckBrandSlug200Response.md)>


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
| **401** | Default Response |  -  |
| **403** | Default Response |  -  |


<a id="APIcheckBrandSlugRequest"></a>
## APIcheckBrandSlugRequest
### Properties

|     Name      |    Type       | Description   |     Notes    |
| ------------- | ------------- | ------------- | -------------|
| **orgId** | **String** | Organization ID | |
| **slug** | **String** | Brand slug to check | |



## createOrgBrand

> ListOrgBrands200ResponseDataInner createOrgBrand(createOrgBrandRequest)

Create brand

Creates a brand (sub-account) in the organization. The slug is derived from the name when omitted. Requires a plan that includes brands.

### Example

```java
// Import classes:
import com.zippendo.sdk.ApiClient;
import com.zippendo.sdk.ApiException;
import com.zippendo.sdk.Configuration;
import com.zippendo.sdk.auth.*;
import com.zippendo.sdk.models.*;
import com.zippendo.sdk.api.BrandsApi;
import com.zippendo.sdk.api.BrandsApi.*;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.zippendo.com");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        BrandsApi apiInstance = new BrandsApi(defaultClient);
        String orgId = "org_8f3kd92ld0"; // String | Organization ID
        CreateOrgBrandRequest createOrgBrandRequest = new CreateOrgBrandRequest(); // CreateOrgBrandRequest | 
        try {
            APIcreateOrgBrandRequest request = APIcreateOrgBrandRequest.newBuilder()
                .orgId(orgId)
                .createOrgBrandRequest(createOrgBrandRequest)
                .build();
            ListOrgBrands200ResponseDataInner result = apiInstance.createOrgBrand(request);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling BrandsApi#createOrgBrand");
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
| createOrgBrandRequest | [**APIcreateOrgBrandRequest**](BrandsApi.md#APIcreateOrgBrandRequest)|-|-|

### Return type

[**ListOrgBrands200ResponseDataInner**](ListOrgBrands200ResponseDataInner.md)


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
| **409** | Default Response |  -  |

## createOrgBrandWithHttpInfo

> ApiResponse<ListOrgBrands200ResponseDataInner> createOrgBrandWithHttpInfo(createOrgBrandRequest)

Create brand

Creates a brand (sub-account) in the organization. The slug is derived from the name when omitted. Requires a plan that includes brands.

### Example

```java
// Import classes:
import com.zippendo.sdk.ApiClient;
import com.zippendo.sdk.ApiException;
import com.zippendo.sdk.ApiResponse;
import com.zippendo.sdk.Configuration;
import com.zippendo.sdk.auth.*;
import com.zippendo.sdk.models.*;
import com.zippendo.sdk.api.BrandsApi;
import com.zippendo.sdk.api.BrandsApi.*;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.zippendo.com");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        BrandsApi apiInstance = new BrandsApi(defaultClient);
        String orgId = "org_8f3kd92ld0"; // String | Organization ID
        CreateOrgBrandRequest createOrgBrandRequest = new CreateOrgBrandRequest(); // CreateOrgBrandRequest | 
        try {
            APIcreateOrgBrandRequest request = APIcreateOrgBrandRequest.newBuilder()
                .orgId(orgId)
                .createOrgBrandRequest(createOrgBrandRequest)
                .build();
            ApiResponse<ListOrgBrands200ResponseDataInner> response = apiInstance.createOrgBrandWithHttpInfo(request);
            System.out.println("Status code: " + response.getStatusCode());
            System.out.println("Response headers: " + response.getHeaders());
            System.out.println("Response body: " + response.getData());
        } catch (ApiException e) {
            System.err.println("Exception when calling BrandsApi#createOrgBrand");
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
| createOrgBrandRequest | [**APIcreateOrgBrandRequest**](BrandsApi.md#APIcreateOrgBrandRequest)|-|-|

### Return type

ApiResponse<[**ListOrgBrands200ResponseDataInner**](ListOrgBrands200ResponseDataInner.md)>


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
| **409** | Default Response |  -  |


<a id="APIcreateOrgBrandRequest"></a>
## APIcreateOrgBrandRequest
### Properties

|     Name      |    Type       | Description   |     Notes    |
| ------------- | ------------- | ------------- | -------------|
| **orgId** | **String** | Organization ID | |
| **createOrgBrandRequest** | [**CreateOrgBrandRequest**](CreateOrgBrandRequest.md) |  | |



## deleteBrandLogo

> ListOrgBrands200ResponseDataInner deleteBrandLogo(deleteBrandLogoRequest)

Delete brand logo

Removes a brand&#39;s logo. Its documents fall back to the organization&#39;s logo. Requires the brands and customBranding entitlements.

### Example

```java
// Import classes:
import com.zippendo.sdk.ApiClient;
import com.zippendo.sdk.ApiException;
import com.zippendo.sdk.Configuration;
import com.zippendo.sdk.auth.*;
import com.zippendo.sdk.models.*;
import com.zippendo.sdk.api.BrandsApi;
import com.zippendo.sdk.api.BrandsApi.*;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.zippendo.com");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        BrandsApi apiInstance = new BrandsApi(defaultClient);
        String orgId = "org_8f3kd92ld0"; // String | Organization ID
        String brandId = "brnd_8f3kd92ld0"; // String | Brand ID
        try {
            APIdeleteBrandLogoRequest request = APIdeleteBrandLogoRequest.newBuilder()
                .orgId(orgId)
                .brandId(brandId)
                .build();
            ListOrgBrands200ResponseDataInner result = apiInstance.deleteBrandLogo(request);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling BrandsApi#deleteBrandLogo");
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
| deleteBrandLogoRequest | [**APIdeleteBrandLogoRequest**](BrandsApi.md#APIdeleteBrandLogoRequest)|-|-|

### Return type

[**ListOrgBrands200ResponseDataInner**](ListOrgBrands200ResponseDataInner.md)


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

## deleteBrandLogoWithHttpInfo

> ApiResponse<ListOrgBrands200ResponseDataInner> deleteBrandLogoWithHttpInfo(deleteBrandLogoRequest)

Delete brand logo

Removes a brand&#39;s logo. Its documents fall back to the organization&#39;s logo. Requires the brands and customBranding entitlements.

### Example

```java
// Import classes:
import com.zippendo.sdk.ApiClient;
import com.zippendo.sdk.ApiException;
import com.zippendo.sdk.ApiResponse;
import com.zippendo.sdk.Configuration;
import com.zippendo.sdk.auth.*;
import com.zippendo.sdk.models.*;
import com.zippendo.sdk.api.BrandsApi;
import com.zippendo.sdk.api.BrandsApi.*;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.zippendo.com");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        BrandsApi apiInstance = new BrandsApi(defaultClient);
        String orgId = "org_8f3kd92ld0"; // String | Organization ID
        String brandId = "brnd_8f3kd92ld0"; // String | Brand ID
        try {
            APIdeleteBrandLogoRequest request = APIdeleteBrandLogoRequest.newBuilder()
                .orgId(orgId)
                .brandId(brandId)
                .build();
            ApiResponse<ListOrgBrands200ResponseDataInner> response = apiInstance.deleteBrandLogoWithHttpInfo(request);
            System.out.println("Status code: " + response.getStatusCode());
            System.out.println("Response headers: " + response.getHeaders());
            System.out.println("Response body: " + response.getData());
        } catch (ApiException e) {
            System.err.println("Exception when calling BrandsApi#deleteBrandLogo");
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
| deleteBrandLogoRequest | [**APIdeleteBrandLogoRequest**](BrandsApi.md#APIdeleteBrandLogoRequest)|-|-|

### Return type

ApiResponse<[**ListOrgBrands200ResponseDataInner**](ListOrgBrands200ResponseDataInner.md)>


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


<a id="APIdeleteBrandLogoRequest"></a>
## APIdeleteBrandLogoRequest
### Properties

|     Name      |    Type       | Description   |     Notes    |
| ------------- | ------------- | ------------- | -------------|
| **orgId** | **String** | Organization ID | |
| **brandId** | **String** | Brand ID | |



## getBrandLogo

> File getBrandLogo(getBrandLogoRequest)

Get brand logo

Streams the brand&#39;s logo bytes. This is the URL returned as the brand&#39;s &#x60;logoUrl&#x60;.

### Example

```java
// Import classes:
import com.zippendo.sdk.ApiClient;
import com.zippendo.sdk.ApiException;
import com.zippendo.sdk.Configuration;
import com.zippendo.sdk.auth.*;
import com.zippendo.sdk.models.*;
import com.zippendo.sdk.api.BrandsApi;
import com.zippendo.sdk.api.BrandsApi.*;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.zippendo.com");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        BrandsApi apiInstance = new BrandsApi(defaultClient);
        String orgId = "org_8f3kd92ld0"; // String | Organization ID
        String brandId = "brnd_8f3kd92ld0"; // String | Brand ID
        try {
            APIgetBrandLogoRequest request = APIgetBrandLogoRequest.newBuilder()
                .orgId(orgId)
                .brandId(brandId)
                .build();
            File result = apiInstance.getBrandLogo(request);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling BrandsApi#getBrandLogo");
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
| getBrandLogoRequest | [**APIgetBrandLogoRequest**](BrandsApi.md#APIgetBrandLogoRequest)|-|-|

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
| **401** | Default Response |  -  |
| **403** | Default Response |  -  |
| **404** | Default Response |  -  |

## getBrandLogoWithHttpInfo

> ApiResponse<File> getBrandLogoWithHttpInfo(getBrandLogoRequest)

Get brand logo

Streams the brand&#39;s logo bytes. This is the URL returned as the brand&#39;s &#x60;logoUrl&#x60;.

### Example

```java
// Import classes:
import com.zippendo.sdk.ApiClient;
import com.zippendo.sdk.ApiException;
import com.zippendo.sdk.ApiResponse;
import com.zippendo.sdk.Configuration;
import com.zippendo.sdk.auth.*;
import com.zippendo.sdk.models.*;
import com.zippendo.sdk.api.BrandsApi;
import com.zippendo.sdk.api.BrandsApi.*;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.zippendo.com");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        BrandsApi apiInstance = new BrandsApi(defaultClient);
        String orgId = "org_8f3kd92ld0"; // String | Organization ID
        String brandId = "brnd_8f3kd92ld0"; // String | Brand ID
        try {
            APIgetBrandLogoRequest request = APIgetBrandLogoRequest.newBuilder()
                .orgId(orgId)
                .brandId(brandId)
                .build();
            ApiResponse<File> response = apiInstance.getBrandLogoWithHttpInfo(request);
            System.out.println("Status code: " + response.getStatusCode());
            System.out.println("Response headers: " + response.getHeaders());
            System.out.println("Response body: " + response.getData());
        } catch (ApiException e) {
            System.err.println("Exception when calling BrandsApi#getBrandLogo");
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
| getBrandLogoRequest | [**APIgetBrandLogoRequest**](BrandsApi.md#APIgetBrandLogoRequest)|-|-|

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
| **401** | Default Response |  -  |
| **403** | Default Response |  -  |
| **404** | Default Response |  -  |


<a id="APIgetBrandLogoRequest"></a>
## APIgetBrandLogoRequest
### Properties

|     Name      |    Type       | Description   |     Notes    |
| ------------- | ------------- | ------------- | -------------|
| **orgId** | **String** | Organization ID | |
| **brandId** | **String** | Brand ID | |



## getOrgBrand

> ListOrgBrands200ResponseDataInner getOrgBrand(getOrgBrandRequest)

Get brand

Returns a single brand (sub-account) by id.

### Example

```java
// Import classes:
import com.zippendo.sdk.ApiClient;
import com.zippendo.sdk.ApiException;
import com.zippendo.sdk.Configuration;
import com.zippendo.sdk.auth.*;
import com.zippendo.sdk.models.*;
import com.zippendo.sdk.api.BrandsApi;
import com.zippendo.sdk.api.BrandsApi.*;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.zippendo.com");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        BrandsApi apiInstance = new BrandsApi(defaultClient);
        String orgId = "org_8f3kd92ld0"; // String | Organization ID
        String brandId = "brnd_8f3kd92ld0"; // String | Brand ID
        try {
            APIgetOrgBrandRequest request = APIgetOrgBrandRequest.newBuilder()
                .orgId(orgId)
                .brandId(brandId)
                .build();
            ListOrgBrands200ResponseDataInner result = apiInstance.getOrgBrand(request);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling BrandsApi#getOrgBrand");
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
| getOrgBrandRequest | [**APIgetOrgBrandRequest**](BrandsApi.md#APIgetOrgBrandRequest)|-|-|

### Return type

[**ListOrgBrands200ResponseDataInner**](ListOrgBrands200ResponseDataInner.md)


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

## getOrgBrandWithHttpInfo

> ApiResponse<ListOrgBrands200ResponseDataInner> getOrgBrandWithHttpInfo(getOrgBrandRequest)

Get brand

Returns a single brand (sub-account) by id.

### Example

```java
// Import classes:
import com.zippendo.sdk.ApiClient;
import com.zippendo.sdk.ApiException;
import com.zippendo.sdk.ApiResponse;
import com.zippendo.sdk.Configuration;
import com.zippendo.sdk.auth.*;
import com.zippendo.sdk.models.*;
import com.zippendo.sdk.api.BrandsApi;
import com.zippendo.sdk.api.BrandsApi.*;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.zippendo.com");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        BrandsApi apiInstance = new BrandsApi(defaultClient);
        String orgId = "org_8f3kd92ld0"; // String | Organization ID
        String brandId = "brnd_8f3kd92ld0"; // String | Brand ID
        try {
            APIgetOrgBrandRequest request = APIgetOrgBrandRequest.newBuilder()
                .orgId(orgId)
                .brandId(brandId)
                .build();
            ApiResponse<ListOrgBrands200ResponseDataInner> response = apiInstance.getOrgBrandWithHttpInfo(request);
            System.out.println("Status code: " + response.getStatusCode());
            System.out.println("Response headers: " + response.getHeaders());
            System.out.println("Response body: " + response.getData());
        } catch (ApiException e) {
            System.err.println("Exception when calling BrandsApi#getOrgBrand");
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
| getOrgBrandRequest | [**APIgetOrgBrandRequest**](BrandsApi.md#APIgetOrgBrandRequest)|-|-|

### Return type

ApiResponse<[**ListOrgBrands200ResponseDataInner**](ListOrgBrands200ResponseDataInner.md)>


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


<a id="APIgetOrgBrandRequest"></a>
## APIgetOrgBrandRequest
### Properties

|     Name      |    Type       | Description   |     Notes    |
| ------------- | ------------- | ------------- | -------------|
| **orgId** | **String** | Organization ID | |
| **brandId** | **String** | Brand ID | |



## listOrgBrands

> ListOrgBrands200Response listOrgBrands(listOrgBrandsRequest)

List brands

Returns the organization&#39;s brands (sub-accounts). Archived brands are excluded unless &#x60;includeArchived&#x60; is set.

### Example

```java
// Import classes:
import com.zippendo.sdk.ApiClient;
import com.zippendo.sdk.ApiException;
import com.zippendo.sdk.Configuration;
import com.zippendo.sdk.auth.*;
import com.zippendo.sdk.models.*;
import com.zippendo.sdk.api.BrandsApi;
import com.zippendo.sdk.api.BrandsApi.*;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.zippendo.com");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        BrandsApi apiInstance = new BrandsApi(defaultClient);
        String orgId = "org_8f3kd92ld0"; // String | Organization ID
        String includeArchived = "false"; // String | Include archived brands in the response
        try {
            APIlistOrgBrandsRequest request = APIlistOrgBrandsRequest.newBuilder()
                .orgId(orgId)
                .includeArchived(includeArchived)
                .build();
            ListOrgBrands200Response result = apiInstance.listOrgBrands(request);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling BrandsApi#listOrgBrands");
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
| listOrgBrandsRequest | [**APIlistOrgBrandsRequest**](BrandsApi.md#APIlistOrgBrandsRequest)|-|-|

### Return type

[**ListOrgBrands200Response**](ListOrgBrands200Response.md)


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

## listOrgBrandsWithHttpInfo

> ApiResponse<ListOrgBrands200Response> listOrgBrandsWithHttpInfo(listOrgBrandsRequest)

List brands

Returns the organization&#39;s brands (sub-accounts). Archived brands are excluded unless &#x60;includeArchived&#x60; is set.

### Example

```java
// Import classes:
import com.zippendo.sdk.ApiClient;
import com.zippendo.sdk.ApiException;
import com.zippendo.sdk.ApiResponse;
import com.zippendo.sdk.Configuration;
import com.zippendo.sdk.auth.*;
import com.zippendo.sdk.models.*;
import com.zippendo.sdk.api.BrandsApi;
import com.zippendo.sdk.api.BrandsApi.*;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.zippendo.com");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        BrandsApi apiInstance = new BrandsApi(defaultClient);
        String orgId = "org_8f3kd92ld0"; // String | Organization ID
        String includeArchived = "false"; // String | Include archived brands in the response
        try {
            APIlistOrgBrandsRequest request = APIlistOrgBrandsRequest.newBuilder()
                .orgId(orgId)
                .includeArchived(includeArchived)
                .build();
            ApiResponse<ListOrgBrands200Response> response = apiInstance.listOrgBrandsWithHttpInfo(request);
            System.out.println("Status code: " + response.getStatusCode());
            System.out.println("Response headers: " + response.getHeaders());
            System.out.println("Response body: " + response.getData());
        } catch (ApiException e) {
            System.err.println("Exception when calling BrandsApi#listOrgBrands");
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
| listOrgBrandsRequest | [**APIlistOrgBrandsRequest**](BrandsApi.md#APIlistOrgBrandsRequest)|-|-|

### Return type

ApiResponse<[**ListOrgBrands200Response**](ListOrgBrands200Response.md)>


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


<a id="APIlistOrgBrandsRequest"></a>
## APIlistOrgBrandsRequest
### Properties

|     Name      |    Type       | Description   |     Notes    |
| ------------- | ------------- | ------------- | -------------|
| **orgId** | **String** | Organization ID | |
| **includeArchived** | **String** | Include archived brands in the response | [optional] |



## unarchiveOrgBrand

> ListOrgBrands200ResponseDataInner unarchiveOrgBrand(unarchiveOrgBrandRequest)

Unarchive brand

Restores an archived brand so it appears in the brand switcher again.

### Example

```java
// Import classes:
import com.zippendo.sdk.ApiClient;
import com.zippendo.sdk.ApiException;
import com.zippendo.sdk.Configuration;
import com.zippendo.sdk.auth.*;
import com.zippendo.sdk.models.*;
import com.zippendo.sdk.api.BrandsApi;
import com.zippendo.sdk.api.BrandsApi.*;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.zippendo.com");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        BrandsApi apiInstance = new BrandsApi(defaultClient);
        String orgId = "org_8f3kd92ld0"; // String | Organization ID
        String brandId = "brnd_8f3kd92ld0"; // String | Brand ID
        try {
            APIunarchiveOrgBrandRequest request = APIunarchiveOrgBrandRequest.newBuilder()
                .orgId(orgId)
                .brandId(brandId)
                .build();
            ListOrgBrands200ResponseDataInner result = apiInstance.unarchiveOrgBrand(request);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling BrandsApi#unarchiveOrgBrand");
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
| unarchiveOrgBrandRequest | [**APIunarchiveOrgBrandRequest**](BrandsApi.md#APIunarchiveOrgBrandRequest)|-|-|

### Return type

[**ListOrgBrands200ResponseDataInner**](ListOrgBrands200ResponseDataInner.md)


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

## unarchiveOrgBrandWithHttpInfo

> ApiResponse<ListOrgBrands200ResponseDataInner> unarchiveOrgBrandWithHttpInfo(unarchiveOrgBrandRequest)

Unarchive brand

Restores an archived brand so it appears in the brand switcher again.

### Example

```java
// Import classes:
import com.zippendo.sdk.ApiClient;
import com.zippendo.sdk.ApiException;
import com.zippendo.sdk.ApiResponse;
import com.zippendo.sdk.Configuration;
import com.zippendo.sdk.auth.*;
import com.zippendo.sdk.models.*;
import com.zippendo.sdk.api.BrandsApi;
import com.zippendo.sdk.api.BrandsApi.*;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.zippendo.com");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        BrandsApi apiInstance = new BrandsApi(defaultClient);
        String orgId = "org_8f3kd92ld0"; // String | Organization ID
        String brandId = "brnd_8f3kd92ld0"; // String | Brand ID
        try {
            APIunarchiveOrgBrandRequest request = APIunarchiveOrgBrandRequest.newBuilder()
                .orgId(orgId)
                .brandId(brandId)
                .build();
            ApiResponse<ListOrgBrands200ResponseDataInner> response = apiInstance.unarchiveOrgBrandWithHttpInfo(request);
            System.out.println("Status code: " + response.getStatusCode());
            System.out.println("Response headers: " + response.getHeaders());
            System.out.println("Response body: " + response.getData());
        } catch (ApiException e) {
            System.err.println("Exception when calling BrandsApi#unarchiveOrgBrand");
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
| unarchiveOrgBrandRequest | [**APIunarchiveOrgBrandRequest**](BrandsApi.md#APIunarchiveOrgBrandRequest)|-|-|

### Return type

ApiResponse<[**ListOrgBrands200ResponseDataInner**](ListOrgBrands200ResponseDataInner.md)>


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


<a id="APIunarchiveOrgBrandRequest"></a>
## APIunarchiveOrgBrandRequest
### Properties

|     Name      |    Type       | Description   |     Notes    |
| ------------- | ------------- | ------------- | -------------|
| **orgId** | **String** | Organization ID | |
| **brandId** | **String** | Brand ID | |



## updateOrgBrand

> ListOrgBrands200ResponseDataInner updateOrgBrand(updateOrgBrandRequest)

Update brand

Updates a brand&#39;s name, slug, identity overrides (company name, VAT, customs, address) and document colors. Null clears an override so the organization&#39;s value applies again.

### Example

```java
// Import classes:
import com.zippendo.sdk.ApiClient;
import com.zippendo.sdk.ApiException;
import com.zippendo.sdk.Configuration;
import com.zippendo.sdk.auth.*;
import com.zippendo.sdk.models.*;
import com.zippendo.sdk.api.BrandsApi;
import com.zippendo.sdk.api.BrandsApi.*;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.zippendo.com");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        BrandsApi apiInstance = new BrandsApi(defaultClient);
        String orgId = "org_8f3kd92ld0"; // String | Organization ID
        String brandId = "brnd_8f3kd92ld0"; // String | Brand ID
        UpdateOrgBrandRequest updateOrgBrandRequest = new UpdateOrgBrandRequest(); // UpdateOrgBrandRequest | 
        try {
            APIupdateOrgBrandRequest request = APIupdateOrgBrandRequest.newBuilder()
                .orgId(orgId)
                .brandId(brandId)
                .updateOrgBrandRequest(updateOrgBrandRequest)
                .build();
            ListOrgBrands200ResponseDataInner result = apiInstance.updateOrgBrand(request);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling BrandsApi#updateOrgBrand");
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
| updateOrgBrandRequest | [**APIupdateOrgBrandRequest**](BrandsApi.md#APIupdateOrgBrandRequest)|-|-|

### Return type

[**ListOrgBrands200ResponseDataInner**](ListOrgBrands200ResponseDataInner.md)


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
| **409** | Default Response |  -  |

## updateOrgBrandWithHttpInfo

> ApiResponse<ListOrgBrands200ResponseDataInner> updateOrgBrandWithHttpInfo(updateOrgBrandRequest)

Update brand

Updates a brand&#39;s name, slug, identity overrides (company name, VAT, customs, address) and document colors. Null clears an override so the organization&#39;s value applies again.

### Example

```java
// Import classes:
import com.zippendo.sdk.ApiClient;
import com.zippendo.sdk.ApiException;
import com.zippendo.sdk.ApiResponse;
import com.zippendo.sdk.Configuration;
import com.zippendo.sdk.auth.*;
import com.zippendo.sdk.models.*;
import com.zippendo.sdk.api.BrandsApi;
import com.zippendo.sdk.api.BrandsApi.*;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.zippendo.com");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        BrandsApi apiInstance = new BrandsApi(defaultClient);
        String orgId = "org_8f3kd92ld0"; // String | Organization ID
        String brandId = "brnd_8f3kd92ld0"; // String | Brand ID
        UpdateOrgBrandRequest updateOrgBrandRequest = new UpdateOrgBrandRequest(); // UpdateOrgBrandRequest | 
        try {
            APIupdateOrgBrandRequest request = APIupdateOrgBrandRequest.newBuilder()
                .orgId(orgId)
                .brandId(brandId)
                .updateOrgBrandRequest(updateOrgBrandRequest)
                .build();
            ApiResponse<ListOrgBrands200ResponseDataInner> response = apiInstance.updateOrgBrandWithHttpInfo(request);
            System.out.println("Status code: " + response.getStatusCode());
            System.out.println("Response headers: " + response.getHeaders());
            System.out.println("Response body: " + response.getData());
        } catch (ApiException e) {
            System.err.println("Exception when calling BrandsApi#updateOrgBrand");
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
| updateOrgBrandRequest | [**APIupdateOrgBrandRequest**](BrandsApi.md#APIupdateOrgBrandRequest)|-|-|

### Return type

ApiResponse<[**ListOrgBrands200ResponseDataInner**](ListOrgBrands200ResponseDataInner.md)>


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
| **409** | Default Response |  -  |


<a id="APIupdateOrgBrandRequest"></a>
## APIupdateOrgBrandRequest
### Properties

|     Name      |    Type       | Description   |     Notes    |
| ------------- | ------------- | ------------- | -------------|
| **orgId** | **String** | Organization ID | |
| **brandId** | **String** | Brand ID | |
| **updateOrgBrandRequest** | [**UpdateOrgBrandRequest**](UpdateOrgBrandRequest.md) |  | |



## uploadBrandLogo

> ListOrgBrands200ResponseDataInner uploadBrandLogo(uploadBrandLogoRequest)

Upload brand logo

Uploads a brand&#39;s logo as multipart/form-data. Accepts PNG, JPG or WEBP up to 5MB and 4096×4096px; the image is re-encoded and stored. Documents for this brand&#39;s shipments use it instead of the organization&#39;s logo. Requires the brands and customBranding entitlements.

### Example

```java
// Import classes:
import com.zippendo.sdk.ApiClient;
import com.zippendo.sdk.ApiException;
import com.zippendo.sdk.Configuration;
import com.zippendo.sdk.auth.*;
import com.zippendo.sdk.models.*;
import com.zippendo.sdk.api.BrandsApi;
import com.zippendo.sdk.api.BrandsApi.*;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.zippendo.com");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        BrandsApi apiInstance = new BrandsApi(defaultClient);
        String orgId = "org_8f3kd92ld0"; // String | Organization ID
        String brandId = "brnd_8f3kd92ld0"; // String | Brand ID
        File _file = new File("/path/to/file"); // File | Image file (PNG, JPG, or WEBP)
        try {
            APIuploadBrandLogoRequest request = APIuploadBrandLogoRequest.newBuilder()
                .orgId(orgId)
                .brandId(brandId)
                ._file(_file)
                .build();
            ListOrgBrands200ResponseDataInner result = apiInstance.uploadBrandLogo(request);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling BrandsApi#uploadBrandLogo");
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
| uploadBrandLogoRequest | [**APIuploadBrandLogoRequest**](BrandsApi.md#APIuploadBrandLogoRequest)|-|-|

### Return type

[**ListOrgBrands200ResponseDataInner**](ListOrgBrands200ResponseDataInner.md)


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

## uploadBrandLogoWithHttpInfo

> ApiResponse<ListOrgBrands200ResponseDataInner> uploadBrandLogoWithHttpInfo(uploadBrandLogoRequest)

Upload brand logo

Uploads a brand&#39;s logo as multipart/form-data. Accepts PNG, JPG or WEBP up to 5MB and 4096×4096px; the image is re-encoded and stored. Documents for this brand&#39;s shipments use it instead of the organization&#39;s logo. Requires the brands and customBranding entitlements.

### Example

```java
// Import classes:
import com.zippendo.sdk.ApiClient;
import com.zippendo.sdk.ApiException;
import com.zippendo.sdk.ApiResponse;
import com.zippendo.sdk.Configuration;
import com.zippendo.sdk.auth.*;
import com.zippendo.sdk.models.*;
import com.zippendo.sdk.api.BrandsApi;
import com.zippendo.sdk.api.BrandsApi.*;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.zippendo.com");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        BrandsApi apiInstance = new BrandsApi(defaultClient);
        String orgId = "org_8f3kd92ld0"; // String | Organization ID
        String brandId = "brnd_8f3kd92ld0"; // String | Brand ID
        File _file = new File("/path/to/file"); // File | Image file (PNG, JPG, or WEBP)
        try {
            APIuploadBrandLogoRequest request = APIuploadBrandLogoRequest.newBuilder()
                .orgId(orgId)
                .brandId(brandId)
                ._file(_file)
                .build();
            ApiResponse<ListOrgBrands200ResponseDataInner> response = apiInstance.uploadBrandLogoWithHttpInfo(request);
            System.out.println("Status code: " + response.getStatusCode());
            System.out.println("Response headers: " + response.getHeaders());
            System.out.println("Response body: " + response.getData());
        } catch (ApiException e) {
            System.err.println("Exception when calling BrandsApi#uploadBrandLogo");
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
| uploadBrandLogoRequest | [**APIuploadBrandLogoRequest**](BrandsApi.md#APIuploadBrandLogoRequest)|-|-|

### Return type

ApiResponse<[**ListOrgBrands200ResponseDataInner**](ListOrgBrands200ResponseDataInner.md)>


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


<a id="APIuploadBrandLogoRequest"></a>
## APIuploadBrandLogoRequest
### Properties

|     Name      |    Type       | Description   |     Notes    |
| ------------- | ------------- | ------------- | -------------|
| **orgId** | **String** | Organization ID | |
| **brandId** | **String** | Brand ID | |
| **_file** | **File** | Image file (PNG, JPG, or WEBP) | |


