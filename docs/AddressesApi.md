# AddressesApi

All URIs are relative to *https://api.zippendo.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**createAddress**](AddressesApi.md#createAddress) | **POST** /orgs/{orgId}/addresses | Create address |
| [**createAddressWithHttpInfo**](AddressesApi.md#createAddressWithHttpInfo) | **POST** /orgs/{orgId}/addresses | Create address |
| [**deleteAddress**](AddressesApi.md#deleteAddress) | **DELETE** /orgs/{orgId}/addresses/{addressId} | Delete address |
| [**deleteAddressWithHttpInfo**](AddressesApi.md#deleteAddressWithHttpInfo) | **DELETE** /orgs/{orgId}/addresses/{addressId} | Delete address |
| [**getAddress**](AddressesApi.md#getAddress) | **GET** /orgs/{orgId}/addresses/{addressId} | Get address |
| [**getAddressWithHttpInfo**](AddressesApi.md#getAddressWithHttpInfo) | **GET** /orgs/{orgId}/addresses/{addressId} | Get address |
| [**listAddresses**](AddressesApi.md#listAddresses) | **GET** /orgs/{orgId}/addresses | List addresses |
| [**listAddressesWithHttpInfo**](AddressesApi.md#listAddressesWithHttpInfo) | **GET** /orgs/{orgId}/addresses | List addresses |
| [**updateAddress**](AddressesApi.md#updateAddress) | **PUT** /orgs/{orgId}/addresses/{addressId} | Update address |
| [**updateAddressWithHttpInfo**](AddressesApi.md#updateAddressWithHttpInfo) | **PUT** /orgs/{orgId}/addresses/{addressId} | Update address |



## createAddress

> ListAddresses200ResponseDataInner createAddress(createAddressRequest)

Create address

Creates a new sender, pickup or return address for the organization.

### Example

```java
// Import classes:
import com.zippendo.sdk.ApiClient;
import com.zippendo.sdk.ApiException;
import com.zippendo.sdk.Configuration;
import com.zippendo.sdk.auth.*;
import com.zippendo.sdk.models.*;
import com.zippendo.sdk.api.AddressesApi;
import com.zippendo.sdk.api.AddressesApi.*;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.zippendo.com");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        AddressesApi apiInstance = new AddressesApi(defaultClient);
        String orgId = "org_01HZX9K2QF"; // String | Organization ID
        CreateAddressRequest createAddressRequest = new CreateAddressRequest(); // CreateAddressRequest | 
        try {
            APIcreateAddressRequest request = APIcreateAddressRequest.newBuilder()
                .orgId(orgId)
                .createAddressRequest(createAddressRequest)
                .build();
            ListAddresses200ResponseDataInner result = apiInstance.createAddress(request);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling AddressesApi#createAddress");
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
| createAddressRequest | [**APIcreateAddressRequest**](AddressesApi.md#APIcreateAddressRequest)|-|-|

### Return type

[**ListAddresses200ResponseDataInner**](ListAddresses200ResponseDataInner.md)


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

## createAddressWithHttpInfo

> ApiResponse<ListAddresses200ResponseDataInner> createAddressWithHttpInfo(createAddressRequest)

Create address

Creates a new sender, pickup or return address for the organization.

### Example

```java
// Import classes:
import com.zippendo.sdk.ApiClient;
import com.zippendo.sdk.ApiException;
import com.zippendo.sdk.ApiResponse;
import com.zippendo.sdk.Configuration;
import com.zippendo.sdk.auth.*;
import com.zippendo.sdk.models.*;
import com.zippendo.sdk.api.AddressesApi;
import com.zippendo.sdk.api.AddressesApi.*;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.zippendo.com");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        AddressesApi apiInstance = new AddressesApi(defaultClient);
        String orgId = "org_01HZX9K2QF"; // String | Organization ID
        CreateAddressRequest createAddressRequest = new CreateAddressRequest(); // CreateAddressRequest | 
        try {
            APIcreateAddressRequest request = APIcreateAddressRequest.newBuilder()
                .orgId(orgId)
                .createAddressRequest(createAddressRequest)
                .build();
            ApiResponse<ListAddresses200ResponseDataInner> response = apiInstance.createAddressWithHttpInfo(request);
            System.out.println("Status code: " + response.getStatusCode());
            System.out.println("Response headers: " + response.getHeaders());
            System.out.println("Response body: " + response.getData());
        } catch (ApiException e) {
            System.err.println("Exception when calling AddressesApi#createAddress");
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
| createAddressRequest | [**APIcreateAddressRequest**](AddressesApi.md#APIcreateAddressRequest)|-|-|

### Return type

ApiResponse<[**ListAddresses200ResponseDataInner**](ListAddresses200ResponseDataInner.md)>


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


<a id="APIcreateAddressRequest"></a>
## APIcreateAddressRequest
### Properties

|     Name      |    Type       | Description   |     Notes    |
| ------------- | ------------- | ------------- | -------------|
| **orgId** | **String** | Organization ID | |
| **createAddressRequest** | [**CreateAddressRequest**](CreateAddressRequest.md) |  | |



## deleteAddress

> String deleteAddress(deleteAddressRequest)

Delete address

Deletes an address belonging to the organization.

### Example

```java
// Import classes:
import com.zippendo.sdk.ApiClient;
import com.zippendo.sdk.ApiException;
import com.zippendo.sdk.Configuration;
import com.zippendo.sdk.auth.*;
import com.zippendo.sdk.models.*;
import com.zippendo.sdk.api.AddressesApi;
import com.zippendo.sdk.api.AddressesApi.*;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.zippendo.com");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        AddressesApi apiInstance = new AddressesApi(defaultClient);
        String orgId = "org_01HZX9K2QF"; // String | Organization ID
        String addressId = "addr_01HZX9K2QF"; // String | Address ID
        try {
            APIdeleteAddressRequest request = APIdeleteAddressRequest.newBuilder()
                .orgId(orgId)
                .addressId(addressId)
                .build();
            String result = apiInstance.deleteAddress(request);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling AddressesApi#deleteAddress");
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
| deleteAddressRequest | [**APIdeleteAddressRequest**](AddressesApi.md#APIdeleteAddressRequest)|-|-|

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

## deleteAddressWithHttpInfo

> ApiResponse<String> deleteAddressWithHttpInfo(deleteAddressRequest)

Delete address

Deletes an address belonging to the organization.

### Example

```java
// Import classes:
import com.zippendo.sdk.ApiClient;
import com.zippendo.sdk.ApiException;
import com.zippendo.sdk.ApiResponse;
import com.zippendo.sdk.Configuration;
import com.zippendo.sdk.auth.*;
import com.zippendo.sdk.models.*;
import com.zippendo.sdk.api.AddressesApi;
import com.zippendo.sdk.api.AddressesApi.*;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.zippendo.com");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        AddressesApi apiInstance = new AddressesApi(defaultClient);
        String orgId = "org_01HZX9K2QF"; // String | Organization ID
        String addressId = "addr_01HZX9K2QF"; // String | Address ID
        try {
            APIdeleteAddressRequest request = APIdeleteAddressRequest.newBuilder()
                .orgId(orgId)
                .addressId(addressId)
                .build();
            ApiResponse<String> response = apiInstance.deleteAddressWithHttpInfo(request);
            System.out.println("Status code: " + response.getStatusCode());
            System.out.println("Response headers: " + response.getHeaders());
            System.out.println("Response body: " + response.getData());
        } catch (ApiException e) {
            System.err.println("Exception when calling AddressesApi#deleteAddress");
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
| deleteAddressRequest | [**APIdeleteAddressRequest**](AddressesApi.md#APIdeleteAddressRequest)|-|-|

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


<a id="APIdeleteAddressRequest"></a>
## APIdeleteAddressRequest
### Properties

|     Name      |    Type       | Description   |     Notes    |
| ------------- | ------------- | ------------- | -------------|
| **orgId** | **String** | Organization ID | |
| **addressId** | **String** | Address ID | |



## getAddress

> ListAddresses200ResponseDataInner getAddress(getAddressRequest)

Get address

Returns a single address belonging to the organization, identified by its ID.

### Example

```java
// Import classes:
import com.zippendo.sdk.ApiClient;
import com.zippendo.sdk.ApiException;
import com.zippendo.sdk.Configuration;
import com.zippendo.sdk.auth.*;
import com.zippendo.sdk.models.*;
import com.zippendo.sdk.api.AddressesApi;
import com.zippendo.sdk.api.AddressesApi.*;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.zippendo.com");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        AddressesApi apiInstance = new AddressesApi(defaultClient);
        String orgId = "org_01HZX9K2QF"; // String | Organization ID
        String addressId = "addr_01HZX9K2QF"; // String | Address ID
        try {
            APIgetAddressRequest request = APIgetAddressRequest.newBuilder()
                .orgId(orgId)
                .addressId(addressId)
                .build();
            ListAddresses200ResponseDataInner result = apiInstance.getAddress(request);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling AddressesApi#getAddress");
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
| getAddressRequest | [**APIgetAddressRequest**](AddressesApi.md#APIgetAddressRequest)|-|-|

### Return type

[**ListAddresses200ResponseDataInner**](ListAddresses200ResponseDataInner.md)


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

## getAddressWithHttpInfo

> ApiResponse<ListAddresses200ResponseDataInner> getAddressWithHttpInfo(getAddressRequest)

Get address

Returns a single address belonging to the organization, identified by its ID.

### Example

```java
// Import classes:
import com.zippendo.sdk.ApiClient;
import com.zippendo.sdk.ApiException;
import com.zippendo.sdk.ApiResponse;
import com.zippendo.sdk.Configuration;
import com.zippendo.sdk.auth.*;
import com.zippendo.sdk.models.*;
import com.zippendo.sdk.api.AddressesApi;
import com.zippendo.sdk.api.AddressesApi.*;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.zippendo.com");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        AddressesApi apiInstance = new AddressesApi(defaultClient);
        String orgId = "org_01HZX9K2QF"; // String | Organization ID
        String addressId = "addr_01HZX9K2QF"; // String | Address ID
        try {
            APIgetAddressRequest request = APIgetAddressRequest.newBuilder()
                .orgId(orgId)
                .addressId(addressId)
                .build();
            ApiResponse<ListAddresses200ResponseDataInner> response = apiInstance.getAddressWithHttpInfo(request);
            System.out.println("Status code: " + response.getStatusCode());
            System.out.println("Response headers: " + response.getHeaders());
            System.out.println("Response body: " + response.getData());
        } catch (ApiException e) {
            System.err.println("Exception when calling AddressesApi#getAddress");
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
| getAddressRequest | [**APIgetAddressRequest**](AddressesApi.md#APIgetAddressRequest)|-|-|

### Return type

ApiResponse<[**ListAddresses200ResponseDataInner**](ListAddresses200ResponseDataInner.md)>


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


<a id="APIgetAddressRequest"></a>
## APIgetAddressRequest
### Properties

|     Name      |    Type       | Description   |     Notes    |
| ------------- | ------------- | ------------- | -------------|
| **orgId** | **String** | Organization ID | |
| **addressId** | **String** | Address ID | |



## listAddresses

> ListAddresses200Response listAddresses(listAddressesRequest)

List addresses

Returns a paginated list of addresses for the organization, optionally filtered by type.

### Example

```java
// Import classes:
import com.zippendo.sdk.ApiClient;
import com.zippendo.sdk.ApiException;
import com.zippendo.sdk.Configuration;
import com.zippendo.sdk.auth.*;
import com.zippendo.sdk.models.*;
import com.zippendo.sdk.api.AddressesApi;
import com.zippendo.sdk.api.AddressesApi.*;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.zippendo.com");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        AddressesApi apiInstance = new AddressesApi(defaultClient);
        String orgId = "org_01HZX9K2QF"; // String | Organization ID
        Integer page = 1; // Integer | Page number (1-based)
        Integer limit = 20; // Integer | Items per page (max 100)
        String type = "sender"; // String | Filter by address type (sender, pickup, return)
        String countryCode = "DK"; // String | Filter by ISO 3166-1 alpha-2 country code.
        String search = "Copenhagen"; // String | Search by company name, description, contact or city.
        String brandId = "brnd_8f3kd92ld0"; // String | Filter by brand. Pass a brand ID, or \"none\" for records not assigned to any brand.
        String brandScope = "own"; // String | How the brand context narrows this list: \"own\" returns only rows assigned to the current brand (requires a brand session, a brand-bound token, or the X-Zippendo-Brand header), \"shared\" returns only unassigned organization-wide rows, \"both\" (default) returns both. The X-Zippendo-Brand-Scope header supplies a default when the parameter is omitted. For strictly brand-owned records (orders, shipments), a brand-scoped request combined with \"shared\" returns no rows, since those records are never visible organization-wide from within a brand context.
        try {
            APIlistAddressesRequest request = APIlistAddressesRequest.newBuilder()
                .orgId(orgId)
                .page(page)
                .limit(limit)
                .type(type)
                .countryCode(countryCode)
                .search(search)
                .brandId(brandId)
                .brandScope(brandScope)
                .build();
            ListAddresses200Response result = apiInstance.listAddresses(request);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling AddressesApi#listAddresses");
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
| listAddressesRequest | [**APIlistAddressesRequest**](AddressesApi.md#APIlistAddressesRequest)|-|-|

### Return type

[**ListAddresses200Response**](ListAddresses200Response.md)


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

## listAddressesWithHttpInfo

> ApiResponse<ListAddresses200Response> listAddressesWithHttpInfo(listAddressesRequest)

List addresses

Returns a paginated list of addresses for the organization, optionally filtered by type.

### Example

```java
// Import classes:
import com.zippendo.sdk.ApiClient;
import com.zippendo.sdk.ApiException;
import com.zippendo.sdk.ApiResponse;
import com.zippendo.sdk.Configuration;
import com.zippendo.sdk.auth.*;
import com.zippendo.sdk.models.*;
import com.zippendo.sdk.api.AddressesApi;
import com.zippendo.sdk.api.AddressesApi.*;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.zippendo.com");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        AddressesApi apiInstance = new AddressesApi(defaultClient);
        String orgId = "org_01HZX9K2QF"; // String | Organization ID
        Integer page = 1; // Integer | Page number (1-based)
        Integer limit = 20; // Integer | Items per page (max 100)
        String type = "sender"; // String | Filter by address type (sender, pickup, return)
        String countryCode = "DK"; // String | Filter by ISO 3166-1 alpha-2 country code.
        String search = "Copenhagen"; // String | Search by company name, description, contact or city.
        String brandId = "brnd_8f3kd92ld0"; // String | Filter by brand. Pass a brand ID, or \"none\" for records not assigned to any brand.
        String brandScope = "own"; // String | How the brand context narrows this list: \"own\" returns only rows assigned to the current brand (requires a brand session, a brand-bound token, or the X-Zippendo-Brand header), \"shared\" returns only unassigned organization-wide rows, \"both\" (default) returns both. The X-Zippendo-Brand-Scope header supplies a default when the parameter is omitted. For strictly brand-owned records (orders, shipments), a brand-scoped request combined with \"shared\" returns no rows, since those records are never visible organization-wide from within a brand context.
        try {
            APIlistAddressesRequest request = APIlistAddressesRequest.newBuilder()
                .orgId(orgId)
                .page(page)
                .limit(limit)
                .type(type)
                .countryCode(countryCode)
                .search(search)
                .brandId(brandId)
                .brandScope(brandScope)
                .build();
            ApiResponse<ListAddresses200Response> response = apiInstance.listAddressesWithHttpInfo(request);
            System.out.println("Status code: " + response.getStatusCode());
            System.out.println("Response headers: " + response.getHeaders());
            System.out.println("Response body: " + response.getData());
        } catch (ApiException e) {
            System.err.println("Exception when calling AddressesApi#listAddresses");
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
| listAddressesRequest | [**APIlistAddressesRequest**](AddressesApi.md#APIlistAddressesRequest)|-|-|

### Return type

ApiResponse<[**ListAddresses200Response**](ListAddresses200Response.md)>


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


<a id="APIlistAddressesRequest"></a>
## APIlistAddressesRequest
### Properties

|     Name      |    Type       | Description   |     Notes    |
| ------------- | ------------- | ------------- | -------------|
| **orgId** | **String** | Organization ID | |
| **page** | **Integer** | Page number (1-based) | [optional] [default to 1] |
| **limit** | **Integer** | Items per page (max 100) | [optional] [default to 20] |
| **type** | **String** | Filter by address type (sender, pickup, return) | [optional] [enum: sender, pickup, return] |
| **countryCode** | **String** | Filter by ISO 3166-1 alpha-2 country code. | [optional] |
| **search** | **String** | Search by company name, description, contact or city. | [optional] |
| **brandId** | **String** | Filter by brand. Pass a brand ID, or \&quot;none\&quot; for records not assigned to any brand. | [optional] |
| **brandScope** | **String** | How the brand context narrows this list: \&quot;own\&quot; returns only rows assigned to the current brand (requires a brand session, a brand-bound token, or the X-Zippendo-Brand header), \&quot;shared\&quot; returns only unassigned organization-wide rows, \&quot;both\&quot; (default) returns both. The X-Zippendo-Brand-Scope header supplies a default when the parameter is omitted. For strictly brand-owned records (orders, shipments), a brand-scoped request combined with \&quot;shared\&quot; returns no rows, since those records are never visible organization-wide from within a brand context. | [optional] [enum: own, shared, both] |



## updateAddress

> ListAddresses200ResponseDataInner updateAddress(updateAddressRequest)

Update address

Updates an existing address belonging to the organization.

### Example

```java
// Import classes:
import com.zippendo.sdk.ApiClient;
import com.zippendo.sdk.ApiException;
import com.zippendo.sdk.Configuration;
import com.zippendo.sdk.auth.*;
import com.zippendo.sdk.models.*;
import com.zippendo.sdk.api.AddressesApi;
import com.zippendo.sdk.api.AddressesApi.*;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.zippendo.com");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        AddressesApi apiInstance = new AddressesApi(defaultClient);
        String orgId = "org_01HZX9K2QF"; // String | Organization ID
        String addressId = "addr_01HZX9K2QF"; // String | Address ID
        UpdateAddressRequest updateAddressRequest = new UpdateAddressRequest(); // UpdateAddressRequest | 
        try {
            APIupdateAddressRequest request = APIupdateAddressRequest.newBuilder()
                .orgId(orgId)
                .addressId(addressId)
                .updateAddressRequest(updateAddressRequest)
                .build();
            ListAddresses200ResponseDataInner result = apiInstance.updateAddress(request);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling AddressesApi#updateAddress");
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
| updateAddressRequest | [**APIupdateAddressRequest**](AddressesApi.md#APIupdateAddressRequest)|-|-|

### Return type

[**ListAddresses200ResponseDataInner**](ListAddresses200ResponseDataInner.md)


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

## updateAddressWithHttpInfo

> ApiResponse<ListAddresses200ResponseDataInner> updateAddressWithHttpInfo(updateAddressRequest)

Update address

Updates an existing address belonging to the organization.

### Example

```java
// Import classes:
import com.zippendo.sdk.ApiClient;
import com.zippendo.sdk.ApiException;
import com.zippendo.sdk.ApiResponse;
import com.zippendo.sdk.Configuration;
import com.zippendo.sdk.auth.*;
import com.zippendo.sdk.models.*;
import com.zippendo.sdk.api.AddressesApi;
import com.zippendo.sdk.api.AddressesApi.*;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.zippendo.com");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        AddressesApi apiInstance = new AddressesApi(defaultClient);
        String orgId = "org_01HZX9K2QF"; // String | Organization ID
        String addressId = "addr_01HZX9K2QF"; // String | Address ID
        UpdateAddressRequest updateAddressRequest = new UpdateAddressRequest(); // UpdateAddressRequest | 
        try {
            APIupdateAddressRequest request = APIupdateAddressRequest.newBuilder()
                .orgId(orgId)
                .addressId(addressId)
                .updateAddressRequest(updateAddressRequest)
                .build();
            ApiResponse<ListAddresses200ResponseDataInner> response = apiInstance.updateAddressWithHttpInfo(request);
            System.out.println("Status code: " + response.getStatusCode());
            System.out.println("Response headers: " + response.getHeaders());
            System.out.println("Response body: " + response.getData());
        } catch (ApiException e) {
            System.err.println("Exception when calling AddressesApi#updateAddress");
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
| updateAddressRequest | [**APIupdateAddressRequest**](AddressesApi.md#APIupdateAddressRequest)|-|-|

### Return type

ApiResponse<[**ListAddresses200ResponseDataInner**](ListAddresses200ResponseDataInner.md)>


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


<a id="APIupdateAddressRequest"></a>
## APIupdateAddressRequest
### Properties

|     Name      |    Type       | Description   |     Notes    |
| ------------- | ------------- | ------------- | -------------|
| **orgId** | **String** | Organization ID | |
| **addressId** | **String** | Address ID | |
| **updateAddressRequest** | [**UpdateAddressRequest**](UpdateAddressRequest.md) |  | |


