# ShipmentsApi

All URIs are relative to *https://api.zippendo.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**batchSendShipments**](ShipmentsApi.md#batchSendShipments) | **POST** /orgs/{orgId}/shipments/batch-send | Batch send shipments |
| [**batchSendShipmentsWithHttpInfo**](ShipmentsApi.md#batchSendShipmentsWithHttpInfo) | **POST** /orgs/{orgId}/shipments/batch-send | Batch send shipments |
| [**batchSplitShipment**](ShipmentsApi.md#batchSplitShipment) | **POST** /orgs/{orgId}/shipments/{shipmentId}/batch-split-shipment | Batch split shipment |
| [**batchSplitShipmentWithHttpInfo**](ShipmentsApi.md#batchSplitShipmentWithHttpInfo) | **POST** /orgs/{orgId}/shipments/{shipmentId}/batch-split-shipment | Batch split shipment |
| [**createReturnShipment**](ShipmentsApi.md#createReturnShipment) | **POST** /orgs/{orgId}/shipments/{shipmentId}/create-return | Create return shipment |
| [**createReturnShipmentWithHttpInfo**](ShipmentsApi.md#createReturnShipmentWithHttpInfo) | **POST** /orgs/{orgId}/shipments/{shipmentId}/create-return | Create return shipment |
| [**createShipment**](ShipmentsApi.md#createShipment) | **POST** /orgs/{orgId}/shipments | Create shipment |
| [**createShipmentWithHttpInfo**](ShipmentsApi.md#createShipmentWithHttpInfo) | **POST** /orgs/{orgId}/shipments | Create shipment |
| [**deleteShipment**](ShipmentsApi.md#deleteShipment) | **DELETE** /orgs/{orgId}/shipments/{shipmentId} | Delete shipment |
| [**deleteShipmentWithHttpInfo**](ShipmentsApi.md#deleteShipmentWithHttpInfo) | **DELETE** /orgs/{orgId}/shipments/{shipmentId} | Delete shipment |
| [**fetchShipmentLabel**](ShipmentsApi.md#fetchShipmentLabel) | **POST** /orgs/{orgId}/shipments/{shipmentId}/fetch-label | Fetch missing label |
| [**fetchShipmentLabelWithHttpInfo**](ShipmentsApi.md#fetchShipmentLabelWithHttpInfo) | **POST** /orgs/{orgId}/shipments/{shipmentId}/fetch-label | Fetch missing label |
| [**getShipment**](ShipmentsApi.md#getShipment) | **GET** /orgs/{orgId}/shipments/{shipmentId} | Get shipment |
| [**getShipmentWithHttpInfo**](ShipmentsApi.md#getShipmentWithHttpInfo) | **GET** /orgs/{orgId}/shipments/{shipmentId} | Get shipment |
| [**getShipmentDocumentContent**](ShipmentsApi.md#getShipmentDocumentContent) | **GET** /orgs/{orgId}/shipments/{shipmentId}/documents/{documentId}/content | Download shipment document |
| [**getShipmentDocumentContentWithHttpInfo**](ShipmentsApi.md#getShipmentDocumentContentWithHttpInfo) | **GET** /orgs/{orgId}/shipments/{shipmentId}/documents/{documentId}/content | Download shipment document |
| [**listShipments**](ShipmentsApi.md#listShipments) | **GET** /orgs/{orgId}/shipments | List shipments |
| [**listShipmentsWithHttpInfo**](ShipmentsApi.md#listShipmentsWithHttpInfo) | **GET** /orgs/{orgId}/shipments | List shipments |
| [**sendShipment**](ShipmentsApi.md#sendShipment) | **POST** /orgs/{orgId}/shipments/{shipmentId}/send | Send shipment |
| [**sendShipmentWithHttpInfo**](ShipmentsApi.md#sendShipmentWithHttpInfo) | **POST** /orgs/{orgId}/shipments/{shipmentId}/send | Send shipment |
| [**splitShipment**](ShipmentsApi.md#splitShipment) | **POST** /orgs/{orgId}/shipments/{shipmentId}/split-shipment | Split shipment |
| [**splitShipmentWithHttpInfo**](ShipmentsApi.md#splitShipmentWithHttpInfo) | **POST** /orgs/{orgId}/shipments/{shipmentId}/split-shipment | Split shipment |
| [**splitShipmentParcel**](ShipmentsApi.md#splitShipmentParcel) | **POST** /orgs/{orgId}/shipments/{shipmentId}/split-parcel | Split parcels |
| [**splitShipmentParcelWithHttpInfo**](ShipmentsApi.md#splitShipmentParcelWithHttpInfo) | **POST** /orgs/{orgId}/shipments/{shipmentId}/split-parcel | Split parcels |
| [**trackShipment**](ShipmentsApi.md#trackShipment) | **GET** /orgs/{orgId}/shipments/{shipmentId}/tracking | Get shipment tracking |
| [**trackShipmentWithHttpInfo**](ShipmentsApi.md#trackShipmentWithHttpInfo) | **GET** /orgs/{orgId}/shipments/{shipmentId}/tracking | Get shipment tracking |
| [**updateShipment**](ShipmentsApi.md#updateShipment) | **PATCH** /orgs/{orgId}/shipments/{shipmentId} | Update shipment |
| [**updateShipmentWithHttpInfo**](ShipmentsApi.md#updateShipmentWithHttpInfo) | **PATCH** /orgs/{orgId}/shipments/{shipmentId} | Update shipment |



## batchSendShipments

> BatchSendShipments200Response batchSendShipments(batchSendShipmentsRequest)

Batch send shipments

Send multiple shipments in &#x60;pending&#x60; or &#x60;error&#x60; status to their carriers in one request. Each shipment is processed independently and reported in &#x60;results&#x60;; a failure on one shipment never aborts the others. Use it to send every shipment on an order at once.

### Example

```java
// Import classes:
import com.zippendo.sdk.ApiClient;
import com.zippendo.sdk.ApiException;
import com.zippendo.sdk.Configuration;
import com.zippendo.sdk.auth.*;
import com.zippendo.sdk.models.*;
import com.zippendo.sdk.api.ShipmentsApi;
import com.zippendo.sdk.api.ShipmentsApi.*;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.zippendo.com");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        ShipmentsApi apiInstance = new ShipmentsApi(defaultClient);
        String orgId = "org_8f3kd92ld0"; // String | Organization ID
        BatchSendShipmentsRequest batchSendShipmentsRequest = new BatchSendShipmentsRequest(); // BatchSendShipmentsRequest | 
        try {
            APIbatchSendShipmentsRequest request = APIbatchSendShipmentsRequest.newBuilder()
                .orgId(orgId)
                .batchSendShipmentsRequest(batchSendShipmentsRequest)
                .build();
            BatchSendShipments200Response result = apiInstance.batchSendShipments(request);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling ShipmentsApi#batchSendShipments");
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
| batchSendShipmentsRequest | [**APIbatchSendShipmentsRequest**](ShipmentsApi.md#APIbatchSendShipmentsRequest)|-|-|

### Return type

[**BatchSendShipments200Response**](BatchSendShipments200Response.md)


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

## batchSendShipmentsWithHttpInfo

> ApiResponse<BatchSendShipments200Response> batchSendShipmentsWithHttpInfo(batchSendShipmentsRequest)

Batch send shipments

Send multiple shipments in &#x60;pending&#x60; or &#x60;error&#x60; status to their carriers in one request. Each shipment is processed independently and reported in &#x60;results&#x60;; a failure on one shipment never aborts the others. Use it to send every shipment on an order at once.

### Example

```java
// Import classes:
import com.zippendo.sdk.ApiClient;
import com.zippendo.sdk.ApiException;
import com.zippendo.sdk.ApiResponse;
import com.zippendo.sdk.Configuration;
import com.zippendo.sdk.auth.*;
import com.zippendo.sdk.models.*;
import com.zippendo.sdk.api.ShipmentsApi;
import com.zippendo.sdk.api.ShipmentsApi.*;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.zippendo.com");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        ShipmentsApi apiInstance = new ShipmentsApi(defaultClient);
        String orgId = "org_8f3kd92ld0"; // String | Organization ID
        BatchSendShipmentsRequest batchSendShipmentsRequest = new BatchSendShipmentsRequest(); // BatchSendShipmentsRequest | 
        try {
            APIbatchSendShipmentsRequest request = APIbatchSendShipmentsRequest.newBuilder()
                .orgId(orgId)
                .batchSendShipmentsRequest(batchSendShipmentsRequest)
                .build();
            ApiResponse<BatchSendShipments200Response> response = apiInstance.batchSendShipmentsWithHttpInfo(request);
            System.out.println("Status code: " + response.getStatusCode());
            System.out.println("Response headers: " + response.getHeaders());
            System.out.println("Response body: " + response.getData());
        } catch (ApiException e) {
            System.err.println("Exception when calling ShipmentsApi#batchSendShipments");
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
| batchSendShipmentsRequest | [**APIbatchSendShipmentsRequest**](ShipmentsApi.md#APIbatchSendShipmentsRequest)|-|-|

### Return type

ApiResponse<[**BatchSendShipments200Response**](BatchSendShipments200Response.md)>


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


<a id="APIbatchSendShipmentsRequest"></a>
## APIbatchSendShipmentsRequest
### Properties

|     Name      |    Type       | Description   |     Notes    |
| ------------- | ------------- | ------------- | -------------|
| **orgId** | **String** | Organization ID | |
| **batchSendShipmentsRequest** | [**BatchSendShipmentsRequest**](BatchSendShipmentsRequest.md) |  | |



## batchSplitShipment

> BatchSplitShipment201Response batchSplitShipment(batchSplitShipmentRequest)

Batch split shipment

Split a parcel into multiple new shipments with per-line quantities in a single atomic operation. Only draft or pending shipments can be split.

### Example

```java
// Import classes:
import com.zippendo.sdk.ApiClient;
import com.zippendo.sdk.ApiException;
import com.zippendo.sdk.Configuration;
import com.zippendo.sdk.auth.*;
import com.zippendo.sdk.models.*;
import com.zippendo.sdk.api.ShipmentsApi;
import com.zippendo.sdk.api.ShipmentsApi.*;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.zippendo.com");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        ShipmentsApi apiInstance = new ShipmentsApi(defaultClient);
        String orgId = "org_1a2b3c4d"; // String | Organization identifier.
        String shipmentId = "shp_4d9e7a2f"; // String | Shipment identifier.
        BatchSplitShipmentRequest batchSplitShipmentRequest = new BatchSplitShipmentRequest(); // BatchSplitShipmentRequest | 
        try {
            APIbatchSplitShipmentRequest request = APIbatchSplitShipmentRequest.newBuilder()
                .orgId(orgId)
                .shipmentId(shipmentId)
                .batchSplitShipmentRequest(batchSplitShipmentRequest)
                .build();
            BatchSplitShipment201Response result = apiInstance.batchSplitShipment(request);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling ShipmentsApi#batchSplitShipment");
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
| batchSplitShipmentRequest | [**APIbatchSplitShipmentRequest**](ShipmentsApi.md#APIbatchSplitShipmentRequest)|-|-|

### Return type

[**BatchSplitShipment201Response**](BatchSplitShipment201Response.md)


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

## batchSplitShipmentWithHttpInfo

> ApiResponse<BatchSplitShipment201Response> batchSplitShipmentWithHttpInfo(batchSplitShipmentRequest)

Batch split shipment

Split a parcel into multiple new shipments with per-line quantities in a single atomic operation. Only draft or pending shipments can be split.

### Example

```java
// Import classes:
import com.zippendo.sdk.ApiClient;
import com.zippendo.sdk.ApiException;
import com.zippendo.sdk.ApiResponse;
import com.zippendo.sdk.Configuration;
import com.zippendo.sdk.auth.*;
import com.zippendo.sdk.models.*;
import com.zippendo.sdk.api.ShipmentsApi;
import com.zippendo.sdk.api.ShipmentsApi.*;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.zippendo.com");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        ShipmentsApi apiInstance = new ShipmentsApi(defaultClient);
        String orgId = "org_1a2b3c4d"; // String | Organization identifier.
        String shipmentId = "shp_4d9e7a2f"; // String | Shipment identifier.
        BatchSplitShipmentRequest batchSplitShipmentRequest = new BatchSplitShipmentRequest(); // BatchSplitShipmentRequest | 
        try {
            APIbatchSplitShipmentRequest request = APIbatchSplitShipmentRequest.newBuilder()
                .orgId(orgId)
                .shipmentId(shipmentId)
                .batchSplitShipmentRequest(batchSplitShipmentRequest)
                .build();
            ApiResponse<BatchSplitShipment201Response> response = apiInstance.batchSplitShipmentWithHttpInfo(request);
            System.out.println("Status code: " + response.getStatusCode());
            System.out.println("Response headers: " + response.getHeaders());
            System.out.println("Response body: " + response.getData());
        } catch (ApiException e) {
            System.err.println("Exception when calling ShipmentsApi#batchSplitShipment");
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
| batchSplitShipmentRequest | [**APIbatchSplitShipmentRequest**](ShipmentsApi.md#APIbatchSplitShipmentRequest)|-|-|

### Return type

ApiResponse<[**BatchSplitShipment201Response**](BatchSplitShipment201Response.md)>


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


<a id="APIbatchSplitShipmentRequest"></a>
## APIbatchSplitShipmentRequest
### Properties

|     Name      |    Type       | Description   |     Notes    |
| ------------- | ------------- | ------------- | -------------|
| **orgId** | **String** | Organization identifier. | |
| **shipmentId** | **String** | Shipment identifier. | |
| **batchSplitShipmentRequest** | [**BatchSplitShipmentRequest**](BatchSplitShipmentRequest.md) |  | |



## createReturnShipment

> CreateShipment201Response createReturnShipment(createReturnShipmentRequest)

Create return shipment

Create and auto-send a return shipment from a dispatched outbound shipment with swapped sender/receiver. Requires a configured return shipping rule. The return is returned with the outcome of sending it: &#x60;dispatched&#x60;, or &#x60;error&#x60; with the carrier&#39;s reasons in &#x60;errors&#x60;. Returns 409 while a return for the same shipment is already being created.

### Example

```java
// Import classes:
import com.zippendo.sdk.ApiClient;
import com.zippendo.sdk.ApiException;
import com.zippendo.sdk.Configuration;
import com.zippendo.sdk.auth.*;
import com.zippendo.sdk.models.*;
import com.zippendo.sdk.api.ShipmentsApi;
import com.zippendo.sdk.api.ShipmentsApi.*;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.zippendo.com");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        ShipmentsApi apiInstance = new ShipmentsApi(defaultClient);
        String orgId = "org_1a2b3c4d"; // String | Organization identifier.
        String shipmentId = "shp_4d9e7a2f"; // String | Shipment identifier.
        try {
            APIcreateReturnShipmentRequest request = APIcreateReturnShipmentRequest.newBuilder()
                .orgId(orgId)
                .shipmentId(shipmentId)
                .build();
            CreateShipment201Response result = apiInstance.createReturnShipment(request);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling ShipmentsApi#createReturnShipment");
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
| createReturnShipmentRequest | [**APIcreateReturnShipmentRequest**](ShipmentsApi.md#APIcreateReturnShipmentRequest)|-|-|

### Return type

[**CreateShipment201Response**](CreateShipment201Response.md)


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
| **409** | Default Response |  -  |

## createReturnShipmentWithHttpInfo

> ApiResponse<CreateShipment201Response> createReturnShipmentWithHttpInfo(createReturnShipmentRequest)

Create return shipment

Create and auto-send a return shipment from a dispatched outbound shipment with swapped sender/receiver. Requires a configured return shipping rule. The return is returned with the outcome of sending it: &#x60;dispatched&#x60;, or &#x60;error&#x60; with the carrier&#39;s reasons in &#x60;errors&#x60;. Returns 409 while a return for the same shipment is already being created.

### Example

```java
// Import classes:
import com.zippendo.sdk.ApiClient;
import com.zippendo.sdk.ApiException;
import com.zippendo.sdk.ApiResponse;
import com.zippendo.sdk.Configuration;
import com.zippendo.sdk.auth.*;
import com.zippendo.sdk.models.*;
import com.zippendo.sdk.api.ShipmentsApi;
import com.zippendo.sdk.api.ShipmentsApi.*;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.zippendo.com");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        ShipmentsApi apiInstance = new ShipmentsApi(defaultClient);
        String orgId = "org_1a2b3c4d"; // String | Organization identifier.
        String shipmentId = "shp_4d9e7a2f"; // String | Shipment identifier.
        try {
            APIcreateReturnShipmentRequest request = APIcreateReturnShipmentRequest.newBuilder()
                .orgId(orgId)
                .shipmentId(shipmentId)
                .build();
            ApiResponse<CreateShipment201Response> response = apiInstance.createReturnShipmentWithHttpInfo(request);
            System.out.println("Status code: " + response.getStatusCode());
            System.out.println("Response headers: " + response.getHeaders());
            System.out.println("Response body: " + response.getData());
        } catch (ApiException e) {
            System.err.println("Exception when calling ShipmentsApi#createReturnShipment");
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
| createReturnShipmentRequest | [**APIcreateReturnShipmentRequest**](ShipmentsApi.md#APIcreateReturnShipmentRequest)|-|-|

### Return type

ApiResponse<[**CreateShipment201Response**](CreateShipment201Response.md)>


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
| **409** | Default Response |  -  |


<a id="APIcreateReturnShipmentRequest"></a>
## APIcreateReturnShipmentRequest
### Properties

|     Name      |    Type       | Description   |     Notes    |
| ------------- | ------------- | ------------- | -------------|
| **orgId** | **String** | Organization identifier. | |
| **shipmentId** | **String** | Shipment identifier. | |



## createShipment

> CreateShipment201Response createShipment(createShipmentRequest)

Create shipment

Create a new shipment for an organization. When orderId is provided, parties and parcels are derived from the order. When shippingRuleId is provided, carrier settings and the sender address derive from the rule.

### Example

```java
// Import classes:
import com.zippendo.sdk.ApiClient;
import com.zippendo.sdk.ApiException;
import com.zippendo.sdk.Configuration;
import com.zippendo.sdk.auth.*;
import com.zippendo.sdk.models.*;
import com.zippendo.sdk.api.ShipmentsApi;
import com.zippendo.sdk.api.ShipmentsApi.*;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.zippendo.com");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        ShipmentsApi apiInstance = new ShipmentsApi(defaultClient);
        String orgId = "org_8f3kd92ld0"; // String | Organization ID
        CreateShipmentRequest createShipmentRequest = new CreateShipmentRequest(); // CreateShipmentRequest | 
        try {
            APIcreateShipmentRequest request = APIcreateShipmentRequest.newBuilder()
                .orgId(orgId)
                .createShipmentRequest(createShipmentRequest)
                .build();
            CreateShipment201Response result = apiInstance.createShipment(request);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling ShipmentsApi#createShipment");
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
| createShipmentRequest | [**APIcreateShipmentRequest**](ShipmentsApi.md#APIcreateShipmentRequest)|-|-|

### Return type

[**CreateShipment201Response**](CreateShipment201Response.md)


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

## createShipmentWithHttpInfo

> ApiResponse<CreateShipment201Response> createShipmentWithHttpInfo(createShipmentRequest)

Create shipment

Create a new shipment for an organization. When orderId is provided, parties and parcels are derived from the order. When shippingRuleId is provided, carrier settings and the sender address derive from the rule.

### Example

```java
// Import classes:
import com.zippendo.sdk.ApiClient;
import com.zippendo.sdk.ApiException;
import com.zippendo.sdk.ApiResponse;
import com.zippendo.sdk.Configuration;
import com.zippendo.sdk.auth.*;
import com.zippendo.sdk.models.*;
import com.zippendo.sdk.api.ShipmentsApi;
import com.zippendo.sdk.api.ShipmentsApi.*;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.zippendo.com");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        ShipmentsApi apiInstance = new ShipmentsApi(defaultClient);
        String orgId = "org_8f3kd92ld0"; // String | Organization ID
        CreateShipmentRequest createShipmentRequest = new CreateShipmentRequest(); // CreateShipmentRequest | 
        try {
            APIcreateShipmentRequest request = APIcreateShipmentRequest.newBuilder()
                .orgId(orgId)
                .createShipmentRequest(createShipmentRequest)
                .build();
            ApiResponse<CreateShipment201Response> response = apiInstance.createShipmentWithHttpInfo(request);
            System.out.println("Status code: " + response.getStatusCode());
            System.out.println("Response headers: " + response.getHeaders());
            System.out.println("Response body: " + response.getData());
        } catch (ApiException e) {
            System.err.println("Exception when calling ShipmentsApi#createShipment");
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
| createShipmentRequest | [**APIcreateShipmentRequest**](ShipmentsApi.md#APIcreateShipmentRequest)|-|-|

### Return type

ApiResponse<[**CreateShipment201Response**](CreateShipment201Response.md)>


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


<a id="APIcreateShipmentRequest"></a>
## APIcreateShipmentRequest
### Properties

|     Name      |    Type       | Description   |     Notes    |
| ------------- | ------------- | ------------- | -------------|
| **orgId** | **String** | Organization ID | |
| **createShipmentRequest** | [**CreateShipmentRequest**](CreateShipmentRequest.md) |  | |



## deleteShipment

> RevokeApiToken200Response deleteShipment(deleteShipmentRequest)

Delete shipment

Delete a shipment. Only shipments in pending status can be deleted.

### Example

```java
// Import classes:
import com.zippendo.sdk.ApiClient;
import com.zippendo.sdk.ApiException;
import com.zippendo.sdk.Configuration;
import com.zippendo.sdk.auth.*;
import com.zippendo.sdk.models.*;
import com.zippendo.sdk.api.ShipmentsApi;
import com.zippendo.sdk.api.ShipmentsApi.*;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.zippendo.com");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        ShipmentsApi apiInstance = new ShipmentsApi(defaultClient);
        String orgId = "org_1a2b3c4d"; // String | Organization identifier.
        String shipmentId = "shp_4d9e7a2f"; // String | Shipment identifier.
        try {
            APIdeleteShipmentRequest request = APIdeleteShipmentRequest.newBuilder()
                .orgId(orgId)
                .shipmentId(shipmentId)
                .build();
            RevokeApiToken200Response result = apiInstance.deleteShipment(request);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling ShipmentsApi#deleteShipment");
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
| deleteShipmentRequest | [**APIdeleteShipmentRequest**](ShipmentsApi.md#APIdeleteShipmentRequest)|-|-|

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

## deleteShipmentWithHttpInfo

> ApiResponse<RevokeApiToken200Response> deleteShipmentWithHttpInfo(deleteShipmentRequest)

Delete shipment

Delete a shipment. Only shipments in pending status can be deleted.

### Example

```java
// Import classes:
import com.zippendo.sdk.ApiClient;
import com.zippendo.sdk.ApiException;
import com.zippendo.sdk.ApiResponse;
import com.zippendo.sdk.Configuration;
import com.zippendo.sdk.auth.*;
import com.zippendo.sdk.models.*;
import com.zippendo.sdk.api.ShipmentsApi;
import com.zippendo.sdk.api.ShipmentsApi.*;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.zippendo.com");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        ShipmentsApi apiInstance = new ShipmentsApi(defaultClient);
        String orgId = "org_1a2b3c4d"; // String | Organization identifier.
        String shipmentId = "shp_4d9e7a2f"; // String | Shipment identifier.
        try {
            APIdeleteShipmentRequest request = APIdeleteShipmentRequest.newBuilder()
                .orgId(orgId)
                .shipmentId(shipmentId)
                .build();
            ApiResponse<RevokeApiToken200Response> response = apiInstance.deleteShipmentWithHttpInfo(request);
            System.out.println("Status code: " + response.getStatusCode());
            System.out.println("Response headers: " + response.getHeaders());
            System.out.println("Response body: " + response.getData());
        } catch (ApiException e) {
            System.err.println("Exception when calling ShipmentsApi#deleteShipment");
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
| deleteShipmentRequest | [**APIdeleteShipmentRequest**](ShipmentsApi.md#APIdeleteShipmentRequest)|-|-|

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


<a id="APIdeleteShipmentRequest"></a>
## APIdeleteShipmentRequest
### Properties

|     Name      |    Type       | Description   |     Notes    |
| ------------- | ------------- | ------------- | -------------|
| **orgId** | **String** | Organization identifier. | |
| **shipmentId** | **String** | Shipment identifier. | |



## fetchShipmentLabel

> CreateShipment201Response fetchShipmentLabel(fetchShipmentLabelRequest)

Fetch missing label

Ask the carrier again for the label of a dispatched shipment whose label could not be downloaded when it was sent (it carries a LABEL_DOWNLOAD_FAILED or CARRIER_BOOKING_UNCONFIRMED warning). Stores the label, clears the warning and returns the shipment.

### Example

```java
// Import classes:
import com.zippendo.sdk.ApiClient;
import com.zippendo.sdk.ApiException;
import com.zippendo.sdk.Configuration;
import com.zippendo.sdk.auth.*;
import com.zippendo.sdk.models.*;
import com.zippendo.sdk.api.ShipmentsApi;
import com.zippendo.sdk.api.ShipmentsApi.*;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.zippendo.com");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        ShipmentsApi apiInstance = new ShipmentsApi(defaultClient);
        String orgId = "org_1a2b3c4d"; // String | Organization identifier.
        String shipmentId = "shp_4d9e7a2f"; // String | Shipment identifier.
        try {
            APIfetchShipmentLabelRequest request = APIfetchShipmentLabelRequest.newBuilder()
                .orgId(orgId)
                .shipmentId(shipmentId)
                .build();
            CreateShipment201Response result = apiInstance.fetchShipmentLabel(request);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling ShipmentsApi#fetchShipmentLabel");
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
| fetchShipmentLabelRequest | [**APIfetchShipmentLabelRequest**](ShipmentsApi.md#APIfetchShipmentLabelRequest)|-|-|

### Return type

[**CreateShipment201Response**](CreateShipment201Response.md)


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
| **409** | Default Response |  -  |
| **422** | Default Response |  -  |

## fetchShipmentLabelWithHttpInfo

> ApiResponse<CreateShipment201Response> fetchShipmentLabelWithHttpInfo(fetchShipmentLabelRequest)

Fetch missing label

Ask the carrier again for the label of a dispatched shipment whose label could not be downloaded when it was sent (it carries a LABEL_DOWNLOAD_FAILED or CARRIER_BOOKING_UNCONFIRMED warning). Stores the label, clears the warning and returns the shipment.

### Example

```java
// Import classes:
import com.zippendo.sdk.ApiClient;
import com.zippendo.sdk.ApiException;
import com.zippendo.sdk.ApiResponse;
import com.zippendo.sdk.Configuration;
import com.zippendo.sdk.auth.*;
import com.zippendo.sdk.models.*;
import com.zippendo.sdk.api.ShipmentsApi;
import com.zippendo.sdk.api.ShipmentsApi.*;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.zippendo.com");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        ShipmentsApi apiInstance = new ShipmentsApi(defaultClient);
        String orgId = "org_1a2b3c4d"; // String | Organization identifier.
        String shipmentId = "shp_4d9e7a2f"; // String | Shipment identifier.
        try {
            APIfetchShipmentLabelRequest request = APIfetchShipmentLabelRequest.newBuilder()
                .orgId(orgId)
                .shipmentId(shipmentId)
                .build();
            ApiResponse<CreateShipment201Response> response = apiInstance.fetchShipmentLabelWithHttpInfo(request);
            System.out.println("Status code: " + response.getStatusCode());
            System.out.println("Response headers: " + response.getHeaders());
            System.out.println("Response body: " + response.getData());
        } catch (ApiException e) {
            System.err.println("Exception when calling ShipmentsApi#fetchShipmentLabel");
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
| fetchShipmentLabelRequest | [**APIfetchShipmentLabelRequest**](ShipmentsApi.md#APIfetchShipmentLabelRequest)|-|-|

### Return type

ApiResponse<[**CreateShipment201Response**](CreateShipment201Response.md)>


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
| **409** | Default Response |  -  |
| **422** | Default Response |  -  |


<a id="APIfetchShipmentLabelRequest"></a>
## APIfetchShipmentLabelRequest
### Properties

|     Name      |    Type       | Description   |     Notes    |
| ------------- | ------------- | ------------- | -------------|
| **orgId** | **String** | Organization identifier. | |
| **shipmentId** | **String** | Shipment identifier. | |



## getShipment

> CreateShipment201Response getShipment(getShipmentRequest)

Get shipment

Retrieve a single shipment by its ID, including parcels, parties, documents and activity.

### Example

```java
// Import classes:
import com.zippendo.sdk.ApiClient;
import com.zippendo.sdk.ApiException;
import com.zippendo.sdk.Configuration;
import com.zippendo.sdk.auth.*;
import com.zippendo.sdk.models.*;
import com.zippendo.sdk.api.ShipmentsApi;
import com.zippendo.sdk.api.ShipmentsApi.*;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.zippendo.com");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        ShipmentsApi apiInstance = new ShipmentsApi(defaultClient);
        String orgId = "org_1a2b3c4d"; // String | Organization identifier.
        String shipmentId = "shp_4d9e7a2f"; // String | Shipment identifier.
        try {
            APIgetShipmentRequest request = APIgetShipmentRequest.newBuilder()
                .orgId(orgId)
                .shipmentId(shipmentId)
                .build();
            CreateShipment201Response result = apiInstance.getShipment(request);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling ShipmentsApi#getShipment");
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
| getShipmentRequest | [**APIgetShipmentRequest**](ShipmentsApi.md#APIgetShipmentRequest)|-|-|

### Return type

[**CreateShipment201Response**](CreateShipment201Response.md)


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

## getShipmentWithHttpInfo

> ApiResponse<CreateShipment201Response> getShipmentWithHttpInfo(getShipmentRequest)

Get shipment

Retrieve a single shipment by its ID, including parcels, parties, documents and activity.

### Example

```java
// Import classes:
import com.zippendo.sdk.ApiClient;
import com.zippendo.sdk.ApiException;
import com.zippendo.sdk.ApiResponse;
import com.zippendo.sdk.Configuration;
import com.zippendo.sdk.auth.*;
import com.zippendo.sdk.models.*;
import com.zippendo.sdk.api.ShipmentsApi;
import com.zippendo.sdk.api.ShipmentsApi.*;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.zippendo.com");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        ShipmentsApi apiInstance = new ShipmentsApi(defaultClient);
        String orgId = "org_1a2b3c4d"; // String | Organization identifier.
        String shipmentId = "shp_4d9e7a2f"; // String | Shipment identifier.
        try {
            APIgetShipmentRequest request = APIgetShipmentRequest.newBuilder()
                .orgId(orgId)
                .shipmentId(shipmentId)
                .build();
            ApiResponse<CreateShipment201Response> response = apiInstance.getShipmentWithHttpInfo(request);
            System.out.println("Status code: " + response.getStatusCode());
            System.out.println("Response headers: " + response.getHeaders());
            System.out.println("Response body: " + response.getData());
        } catch (ApiException e) {
            System.err.println("Exception when calling ShipmentsApi#getShipment");
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
| getShipmentRequest | [**APIgetShipmentRequest**](ShipmentsApi.md#APIgetShipmentRequest)|-|-|

### Return type

ApiResponse<[**CreateShipment201Response**](CreateShipment201Response.md)>


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


<a id="APIgetShipmentRequest"></a>
## APIgetShipmentRequest
### Properties

|     Name      |    Type       | Description   |     Notes    |
| ------------- | ------------- | ------------- | -------------|
| **orgId** | **String** | Organization identifier. | |
| **shipmentId** | **String** | Shipment identifier. | |



## getShipmentDocumentContent

> void getShipmentDocumentContent(getShipmentDocumentContentRequest)

Download shipment document

Streams a shipment document or label file from storage.

### Example

```java
// Import classes:
import com.zippendo.sdk.ApiClient;
import com.zippendo.sdk.ApiException;
import com.zippendo.sdk.Configuration;
import com.zippendo.sdk.auth.*;
import com.zippendo.sdk.models.*;
import com.zippendo.sdk.api.ShipmentsApi;
import com.zippendo.sdk.api.ShipmentsApi.*;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.zippendo.com");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        ShipmentsApi apiInstance = new ShipmentsApi(defaultClient);
        String orgId = "org_1a2b3c4d"; // String | Organization identifier.
        String shipmentId = "shp_4d9e7a2f"; // String | Shipment identifier.
        String documentId = "doc_8f3a2b1c"; // String | Document identifier.
        String disposition = "inline"; // String | Render the document inline (default) or force a download.
        String filename = "label"; // String | Suggested filename (without extension) for attachment downloads.
        try {
            APIgetShipmentDocumentContentRequest request = APIgetShipmentDocumentContentRequest.newBuilder()
                .orgId(orgId)
                .shipmentId(shipmentId)
                .documentId(documentId)
                .disposition(disposition)
                .filename(filename)
                .build();
            apiInstance.getShipmentDocumentContent(request);
        } catch (ApiException e) {
            System.err.println("Exception when calling ShipmentsApi#getShipmentDocumentContent");
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
| getShipmentDocumentContentRequest | [**APIgetShipmentDocumentContentRequest**](ShipmentsApi.md#APIgetShipmentDocumentContentRequest)|-|-|

### Return type


null (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Default Response |  -  |

## getShipmentDocumentContentWithHttpInfo

> ApiResponse<Void> getShipmentDocumentContentWithHttpInfo(getShipmentDocumentContentRequest)

Download shipment document

Streams a shipment document or label file from storage.

### Example

```java
// Import classes:
import com.zippendo.sdk.ApiClient;
import com.zippendo.sdk.ApiException;
import com.zippendo.sdk.ApiResponse;
import com.zippendo.sdk.Configuration;
import com.zippendo.sdk.auth.*;
import com.zippendo.sdk.models.*;
import com.zippendo.sdk.api.ShipmentsApi;
import com.zippendo.sdk.api.ShipmentsApi.*;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.zippendo.com");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        ShipmentsApi apiInstance = new ShipmentsApi(defaultClient);
        String orgId = "org_1a2b3c4d"; // String | Organization identifier.
        String shipmentId = "shp_4d9e7a2f"; // String | Shipment identifier.
        String documentId = "doc_8f3a2b1c"; // String | Document identifier.
        String disposition = "inline"; // String | Render the document inline (default) or force a download.
        String filename = "label"; // String | Suggested filename (without extension) for attachment downloads.
        try {
            APIgetShipmentDocumentContentRequest request = APIgetShipmentDocumentContentRequest.newBuilder()
                .orgId(orgId)
                .shipmentId(shipmentId)
                .documentId(documentId)
                .disposition(disposition)
                .filename(filename)
                .build();
            ApiResponse<Void> response = apiInstance.getShipmentDocumentContentWithHttpInfo(request);
            System.out.println("Status code: " + response.getStatusCode());
            System.out.println("Response headers: " + response.getHeaders());
        } catch (ApiException e) {
            System.err.println("Exception when calling ShipmentsApi#getShipmentDocumentContent");
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
| getShipmentDocumentContentRequest | [**APIgetShipmentDocumentContentRequest**](ShipmentsApi.md#APIgetShipmentDocumentContentRequest)|-|-|

### Return type


ApiResponse<Void>

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Default Response |  -  |


<a id="APIgetShipmentDocumentContentRequest"></a>
## APIgetShipmentDocumentContentRequest
### Properties

|     Name      |    Type       | Description   |     Notes    |
| ------------- | ------------- | ------------- | -------------|
| **orgId** | **String** | Organization identifier. | |
| **shipmentId** | **String** | Shipment identifier. | |
| **documentId** | **String** | Document identifier. | |
| **disposition** | **String** | Render the document inline (default) or force a download. | [optional] [default to inline] [enum: inline, attachment] |
| **filename** | **String** | Suggested filename (without extension) for attachment downloads. | [optional] |



## listShipments

> ListShipments200Response listShipments(listShipmentsRequest)

List shipments

List all shipments for an organization, paginated and ordered by newest first. Accepts an advanced filter definition.

### Example

```java
// Import classes:
import com.zippendo.sdk.ApiClient;
import com.zippendo.sdk.ApiException;
import com.zippendo.sdk.Configuration;
import com.zippendo.sdk.auth.*;
import com.zippendo.sdk.models.*;
import com.zippendo.sdk.api.ShipmentsApi;
import com.zippendo.sdk.api.ShipmentsApi.*;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.zippendo.com");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        ShipmentsApi apiInstance = new ShipmentsApi(defaultClient);
        String orgId = "org_8f3kd92ld0"; // String | Organization ID
        Integer page = 1; // Integer | Page number (1-based)
        Integer limit = 20; // Integer | Items per page (max 100)
        String brandId = "brnd_8f3kd92ld0"; // String | Filter by brand. Pass a brand ID, or \"none\" for records not assigned to any brand.
        String brandScope = "own"; // String | How the brand context narrows this list: \"own\" returns only rows assigned to the current brand (requires a brand session, a brand-bound token, or the X-Zippendo-Brand header), \"shared\" returns only unassigned organization-wide rows, \"both\" (default) returns both. The X-Zippendo-Brand-Scope header supplies a default when the parameter is omitted. For strictly brand-owned records (orders, shipments), a brand-scoped request combined with \"shared\" returns no rows, since those records are never visible organization-wide from within a brand context.
        String status = "draft"; // String | Filter by shipment status.
        String type = "outbound"; // String | Filter by direction.
        String search = "SHIP-1042"; // String | Search by shipment reference or parcel tracking number.
        String filter = "{\"conjunction\":\"and\",\"conditions\":[{\"id\":\"c_1\",\"field\":\"status\",\"operator\":\"in\",\"value\":[\"pending\",\"processing\"]}]}"; // String | Advanced filter as a JSON-encoded definition: a `conjunction` (`and`/`or`) over `conditions`, each `{ id, field, operator, value }` or a nested group. Fields and operators per list are documented under Filtering lists in the API overview. An invalid filter returns 400 `FILTER_INVALID`.
        try {
            APIlistShipmentsRequest request = APIlistShipmentsRequest.newBuilder()
                .orgId(orgId)
                .page(page)
                .limit(limit)
                .brandId(brandId)
                .brandScope(brandScope)
                .status(status)
                .type(type)
                .search(search)
                .filter(filter)
                .build();
            ListShipments200Response result = apiInstance.listShipments(request);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling ShipmentsApi#listShipments");
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
| listShipmentsRequest | [**APIlistShipmentsRequest**](ShipmentsApi.md#APIlistShipmentsRequest)|-|-|

### Return type

[**ListShipments200Response**](ListShipments200Response.md)


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

## listShipmentsWithHttpInfo

> ApiResponse<ListShipments200Response> listShipmentsWithHttpInfo(listShipmentsRequest)

List shipments

List all shipments for an organization, paginated and ordered by newest first. Accepts an advanced filter definition.

### Example

```java
// Import classes:
import com.zippendo.sdk.ApiClient;
import com.zippendo.sdk.ApiException;
import com.zippendo.sdk.ApiResponse;
import com.zippendo.sdk.Configuration;
import com.zippendo.sdk.auth.*;
import com.zippendo.sdk.models.*;
import com.zippendo.sdk.api.ShipmentsApi;
import com.zippendo.sdk.api.ShipmentsApi.*;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.zippendo.com");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        ShipmentsApi apiInstance = new ShipmentsApi(defaultClient);
        String orgId = "org_8f3kd92ld0"; // String | Organization ID
        Integer page = 1; // Integer | Page number (1-based)
        Integer limit = 20; // Integer | Items per page (max 100)
        String brandId = "brnd_8f3kd92ld0"; // String | Filter by brand. Pass a brand ID, or \"none\" for records not assigned to any brand.
        String brandScope = "own"; // String | How the brand context narrows this list: \"own\" returns only rows assigned to the current brand (requires a brand session, a brand-bound token, or the X-Zippendo-Brand header), \"shared\" returns only unassigned organization-wide rows, \"both\" (default) returns both. The X-Zippendo-Brand-Scope header supplies a default when the parameter is omitted. For strictly brand-owned records (orders, shipments), a brand-scoped request combined with \"shared\" returns no rows, since those records are never visible organization-wide from within a brand context.
        String status = "draft"; // String | Filter by shipment status.
        String type = "outbound"; // String | Filter by direction.
        String search = "SHIP-1042"; // String | Search by shipment reference or parcel tracking number.
        String filter = "{\"conjunction\":\"and\",\"conditions\":[{\"id\":\"c_1\",\"field\":\"status\",\"operator\":\"in\",\"value\":[\"pending\",\"processing\"]}]}"; // String | Advanced filter as a JSON-encoded definition: a `conjunction` (`and`/`or`) over `conditions`, each `{ id, field, operator, value }` or a nested group. Fields and operators per list are documented under Filtering lists in the API overview. An invalid filter returns 400 `FILTER_INVALID`.
        try {
            APIlistShipmentsRequest request = APIlistShipmentsRequest.newBuilder()
                .orgId(orgId)
                .page(page)
                .limit(limit)
                .brandId(brandId)
                .brandScope(brandScope)
                .status(status)
                .type(type)
                .search(search)
                .filter(filter)
                .build();
            ApiResponse<ListShipments200Response> response = apiInstance.listShipmentsWithHttpInfo(request);
            System.out.println("Status code: " + response.getStatusCode());
            System.out.println("Response headers: " + response.getHeaders());
            System.out.println("Response body: " + response.getData());
        } catch (ApiException e) {
            System.err.println("Exception when calling ShipmentsApi#listShipments");
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
| listShipmentsRequest | [**APIlistShipmentsRequest**](ShipmentsApi.md#APIlistShipmentsRequest)|-|-|

### Return type

ApiResponse<[**ListShipments200Response**](ListShipments200Response.md)>


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


<a id="APIlistShipmentsRequest"></a>
## APIlistShipmentsRequest
### Properties

|     Name      |    Type       | Description   |     Notes    |
| ------------- | ------------- | ------------- | -------------|
| **orgId** | **String** | Organization ID | |
| **page** | **Integer** | Page number (1-based) | [optional] [default to 1] |
| **limit** | **Integer** | Items per page (max 100) | [optional] [default to 20] |
| **brandId** | **String** | Filter by brand. Pass a brand ID, or \&quot;none\&quot; for records not assigned to any brand. | [optional] |
| **brandScope** | **String** | How the brand context narrows this list: \&quot;own\&quot; returns only rows assigned to the current brand (requires a brand session, a brand-bound token, or the X-Zippendo-Brand header), \&quot;shared\&quot; returns only unassigned organization-wide rows, \&quot;both\&quot; (default) returns both. The X-Zippendo-Brand-Scope header supplies a default when the parameter is omitted. For strictly brand-owned records (orders, shipments), a brand-scoped request combined with \&quot;shared\&quot; returns no rows, since those records are never visible organization-wide from within a brand context. | [optional] [enum: own, shared, both] |
| **status** | **String** | Filter by shipment status. | [optional] [enum: draft, pending, processing, dispatched, partly_dispatched, error, cancelled, on_hold] |
| **type** | **String** | Filter by direction. | [optional] [enum: outbound, inbound] |
| **search** | **String** | Search by shipment reference or parcel tracking number. | [optional] |
| **filter** | **String** | Advanced filter as a JSON-encoded definition: a &#x60;conjunction&#x60; (&#x60;and&#x60;/&#x60;or&#x60;) over &#x60;conditions&#x60;, each &#x60;{ id, field, operator, value }&#x60; or a nested group. Fields and operators per list are documented under Filtering lists in the API overview. An invalid filter returns 400 &#x60;FILTER_INVALID&#x60;. | [optional] |



## sendShipment

> CreateShipment201Response sendShipment(sendShipmentRequest)

Send shipment

Send a shipment in &#x60;pending&#x60; or &#x60;error&#x60; status to its carrier, generating labels and tracking. Returns 422 with the carrier&#39;s errors if sending fails, and 409 while the same shipment is already being sent.

### Example

```java
// Import classes:
import com.zippendo.sdk.ApiClient;
import com.zippendo.sdk.ApiException;
import com.zippendo.sdk.Configuration;
import com.zippendo.sdk.auth.*;
import com.zippendo.sdk.models.*;
import com.zippendo.sdk.api.ShipmentsApi;
import com.zippendo.sdk.api.ShipmentsApi.*;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.zippendo.com");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        ShipmentsApi apiInstance = new ShipmentsApi(defaultClient);
        String orgId = "org_1a2b3c4d"; // String | Organization identifier.
        String shipmentId = "shp_4d9e7a2f"; // String | Shipment identifier.
        try {
            APIsendShipmentRequest request = APIsendShipmentRequest.newBuilder()
                .orgId(orgId)
                .shipmentId(shipmentId)
                .build();
            CreateShipment201Response result = apiInstance.sendShipment(request);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling ShipmentsApi#sendShipment");
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
| sendShipmentRequest | [**APIsendShipmentRequest**](ShipmentsApi.md#APIsendShipmentRequest)|-|-|

### Return type

[**CreateShipment201Response**](CreateShipment201Response.md)


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
| **409** | Default Response |  -  |
| **422** | Default Response |  -  |

## sendShipmentWithHttpInfo

> ApiResponse<CreateShipment201Response> sendShipmentWithHttpInfo(sendShipmentRequest)

Send shipment

Send a shipment in &#x60;pending&#x60; or &#x60;error&#x60; status to its carrier, generating labels and tracking. Returns 422 with the carrier&#39;s errors if sending fails, and 409 while the same shipment is already being sent.

### Example

```java
// Import classes:
import com.zippendo.sdk.ApiClient;
import com.zippendo.sdk.ApiException;
import com.zippendo.sdk.ApiResponse;
import com.zippendo.sdk.Configuration;
import com.zippendo.sdk.auth.*;
import com.zippendo.sdk.models.*;
import com.zippendo.sdk.api.ShipmentsApi;
import com.zippendo.sdk.api.ShipmentsApi.*;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.zippendo.com");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        ShipmentsApi apiInstance = new ShipmentsApi(defaultClient);
        String orgId = "org_1a2b3c4d"; // String | Organization identifier.
        String shipmentId = "shp_4d9e7a2f"; // String | Shipment identifier.
        try {
            APIsendShipmentRequest request = APIsendShipmentRequest.newBuilder()
                .orgId(orgId)
                .shipmentId(shipmentId)
                .build();
            ApiResponse<CreateShipment201Response> response = apiInstance.sendShipmentWithHttpInfo(request);
            System.out.println("Status code: " + response.getStatusCode());
            System.out.println("Response headers: " + response.getHeaders());
            System.out.println("Response body: " + response.getData());
        } catch (ApiException e) {
            System.err.println("Exception when calling ShipmentsApi#sendShipment");
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
| sendShipmentRequest | [**APIsendShipmentRequest**](ShipmentsApi.md#APIsendShipmentRequest)|-|-|

### Return type

ApiResponse<[**CreateShipment201Response**](CreateShipment201Response.md)>


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
| **409** | Default Response |  -  |
| **422** | Default Response |  -  |


<a id="APIsendShipmentRequest"></a>
## APIsendShipmentRequest
### Properties

|     Name      |    Type       | Description   |     Notes    |
| ------------- | ------------- | ------------- | -------------|
| **orgId** | **String** | Organization identifier. | |
| **shipmentId** | **String** | Shipment identifier. | |



## splitShipment

> SplitShipment201Response splitShipment(splitShipmentRequest)

Split shipment

Move order lines from a parcel into a new shipment. Only draft or pending shipments can be split.

### Example

```java
// Import classes:
import com.zippendo.sdk.ApiClient;
import com.zippendo.sdk.ApiException;
import com.zippendo.sdk.Configuration;
import com.zippendo.sdk.auth.*;
import com.zippendo.sdk.models.*;
import com.zippendo.sdk.api.ShipmentsApi;
import com.zippendo.sdk.api.ShipmentsApi.*;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.zippendo.com");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        ShipmentsApi apiInstance = new ShipmentsApi(defaultClient);
        String orgId = "org_1a2b3c4d"; // String | Organization identifier.
        String shipmentId = "shp_4d9e7a2f"; // String | Shipment identifier.
        SplitShipmentRequest splitShipmentRequest = new SplitShipmentRequest(); // SplitShipmentRequest | 
        try {
            APIsplitShipmentRequest request = APIsplitShipmentRequest.newBuilder()
                .orgId(orgId)
                .shipmentId(shipmentId)
                .splitShipmentRequest(splitShipmentRequest)
                .build();
            SplitShipment201Response result = apiInstance.splitShipment(request);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling ShipmentsApi#splitShipment");
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
| splitShipmentRequest | [**APIsplitShipmentRequest**](ShipmentsApi.md#APIsplitShipmentRequest)|-|-|

### Return type

[**SplitShipment201Response**](SplitShipment201Response.md)


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

## splitShipmentWithHttpInfo

> ApiResponse<SplitShipment201Response> splitShipmentWithHttpInfo(splitShipmentRequest)

Split shipment

Move order lines from a parcel into a new shipment. Only draft or pending shipments can be split.

### Example

```java
// Import classes:
import com.zippendo.sdk.ApiClient;
import com.zippendo.sdk.ApiException;
import com.zippendo.sdk.ApiResponse;
import com.zippendo.sdk.Configuration;
import com.zippendo.sdk.auth.*;
import com.zippendo.sdk.models.*;
import com.zippendo.sdk.api.ShipmentsApi;
import com.zippendo.sdk.api.ShipmentsApi.*;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.zippendo.com");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        ShipmentsApi apiInstance = new ShipmentsApi(defaultClient);
        String orgId = "org_1a2b3c4d"; // String | Organization identifier.
        String shipmentId = "shp_4d9e7a2f"; // String | Shipment identifier.
        SplitShipmentRequest splitShipmentRequest = new SplitShipmentRequest(); // SplitShipmentRequest | 
        try {
            APIsplitShipmentRequest request = APIsplitShipmentRequest.newBuilder()
                .orgId(orgId)
                .shipmentId(shipmentId)
                .splitShipmentRequest(splitShipmentRequest)
                .build();
            ApiResponse<SplitShipment201Response> response = apiInstance.splitShipmentWithHttpInfo(request);
            System.out.println("Status code: " + response.getStatusCode());
            System.out.println("Response headers: " + response.getHeaders());
            System.out.println("Response body: " + response.getData());
        } catch (ApiException e) {
            System.err.println("Exception when calling ShipmentsApi#splitShipment");
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
| splitShipmentRequest | [**APIsplitShipmentRequest**](ShipmentsApi.md#APIsplitShipmentRequest)|-|-|

### Return type

ApiResponse<[**SplitShipment201Response**](SplitShipment201Response.md)>


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


<a id="APIsplitShipmentRequest"></a>
## APIsplitShipmentRequest
### Properties

|     Name      |    Type       | Description   |     Notes    |
| ------------- | ------------- | ------------- | -------------|
| **orgId** | **String** | Organization identifier. | |
| **shipmentId** | **String** | Shipment identifier. | |
| **splitShipmentRequest** | [**SplitShipmentRequest**](SplitShipmentRequest.md) |  | |



## splitShipmentParcel

> SplitShipmentParcel200Response splitShipmentParcel(splitShipmentParcelRequest)

Split parcels

Redistribute order lines across parcels within a shipment, moving lines between parcels and creating new ones. Only draft, pending or error shipments can be modified.

### Example

```java
// Import classes:
import com.zippendo.sdk.ApiClient;
import com.zippendo.sdk.ApiException;
import com.zippendo.sdk.Configuration;
import com.zippendo.sdk.auth.*;
import com.zippendo.sdk.models.*;
import com.zippendo.sdk.api.ShipmentsApi;
import com.zippendo.sdk.api.ShipmentsApi.*;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.zippendo.com");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        ShipmentsApi apiInstance = new ShipmentsApi(defaultClient);
        String orgId = "org_1a2b3c4d"; // String | Organization identifier.
        String shipmentId = "shp_4d9e7a2f"; // String | Shipment identifier.
        SplitShipmentParcelRequest splitShipmentParcelRequest = new SplitShipmentParcelRequest(); // SplitShipmentParcelRequest | 
        try {
            APIsplitShipmentParcelRequest request = APIsplitShipmentParcelRequest.newBuilder()
                .orgId(orgId)
                .shipmentId(shipmentId)
                .splitShipmentParcelRequest(splitShipmentParcelRequest)
                .build();
            SplitShipmentParcel200Response result = apiInstance.splitShipmentParcel(request);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling ShipmentsApi#splitShipmentParcel");
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
| splitShipmentParcelRequest | [**APIsplitShipmentParcelRequest**](ShipmentsApi.md#APIsplitShipmentParcelRequest)|-|-|

### Return type

[**SplitShipmentParcel200Response**](SplitShipmentParcel200Response.md)


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

## splitShipmentParcelWithHttpInfo

> ApiResponse<SplitShipmentParcel200Response> splitShipmentParcelWithHttpInfo(splitShipmentParcelRequest)

Split parcels

Redistribute order lines across parcels within a shipment, moving lines between parcels and creating new ones. Only draft, pending or error shipments can be modified.

### Example

```java
// Import classes:
import com.zippendo.sdk.ApiClient;
import com.zippendo.sdk.ApiException;
import com.zippendo.sdk.ApiResponse;
import com.zippendo.sdk.Configuration;
import com.zippendo.sdk.auth.*;
import com.zippendo.sdk.models.*;
import com.zippendo.sdk.api.ShipmentsApi;
import com.zippendo.sdk.api.ShipmentsApi.*;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.zippendo.com");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        ShipmentsApi apiInstance = new ShipmentsApi(defaultClient);
        String orgId = "org_1a2b3c4d"; // String | Organization identifier.
        String shipmentId = "shp_4d9e7a2f"; // String | Shipment identifier.
        SplitShipmentParcelRequest splitShipmentParcelRequest = new SplitShipmentParcelRequest(); // SplitShipmentParcelRequest | 
        try {
            APIsplitShipmentParcelRequest request = APIsplitShipmentParcelRequest.newBuilder()
                .orgId(orgId)
                .shipmentId(shipmentId)
                .splitShipmentParcelRequest(splitShipmentParcelRequest)
                .build();
            ApiResponse<SplitShipmentParcel200Response> response = apiInstance.splitShipmentParcelWithHttpInfo(request);
            System.out.println("Status code: " + response.getStatusCode());
            System.out.println("Response headers: " + response.getHeaders());
            System.out.println("Response body: " + response.getData());
        } catch (ApiException e) {
            System.err.println("Exception when calling ShipmentsApi#splitShipmentParcel");
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
| splitShipmentParcelRequest | [**APIsplitShipmentParcelRequest**](ShipmentsApi.md#APIsplitShipmentParcelRequest)|-|-|

### Return type

ApiResponse<[**SplitShipmentParcel200Response**](SplitShipmentParcel200Response.md)>


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


<a id="APIsplitShipmentParcelRequest"></a>
## APIsplitShipmentParcelRequest
### Properties

|     Name      |    Type       | Description   |     Notes    |
| ------------- | ------------- | ------------- | -------------|
| **orgId** | **String** | Organization identifier. | |
| **shipmentId** | **String** | Shipment identifier. | |
| **splitShipmentParcelRequest** | [**SplitShipmentParcelRequest**](SplitShipmentParcelRequest.md) |  | |



## trackShipment

> TrackShipment200Response trackShipment(trackShipmentRequest)

Get shipment tracking

Retrieve the tracking timeline for a shipment, including current status and all carrier events.

### Example

```java
// Import classes:
import com.zippendo.sdk.ApiClient;
import com.zippendo.sdk.ApiException;
import com.zippendo.sdk.Configuration;
import com.zippendo.sdk.auth.*;
import com.zippendo.sdk.models.*;
import com.zippendo.sdk.api.ShipmentsApi;
import com.zippendo.sdk.api.ShipmentsApi.*;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.zippendo.com");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        ShipmentsApi apiInstance = new ShipmentsApi(defaultClient);
        String orgId = "org_1a2b3c4d"; // String | Organization identifier.
        String shipmentId = "shp_4d9e7a2f"; // String | Shipment identifier.
        try {
            APItrackShipmentRequest request = APItrackShipmentRequest.newBuilder()
                .orgId(orgId)
                .shipmentId(shipmentId)
                .build();
            TrackShipment200Response result = apiInstance.trackShipment(request);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling ShipmentsApi#trackShipment");
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
| trackShipmentRequest | [**APItrackShipmentRequest**](ShipmentsApi.md#APItrackShipmentRequest)|-|-|

### Return type

[**TrackShipment200Response**](TrackShipment200Response.md)


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

## trackShipmentWithHttpInfo

> ApiResponse<TrackShipment200Response> trackShipmentWithHttpInfo(trackShipmentRequest)

Get shipment tracking

Retrieve the tracking timeline for a shipment, including current status and all carrier events.

### Example

```java
// Import classes:
import com.zippendo.sdk.ApiClient;
import com.zippendo.sdk.ApiException;
import com.zippendo.sdk.ApiResponse;
import com.zippendo.sdk.Configuration;
import com.zippendo.sdk.auth.*;
import com.zippendo.sdk.models.*;
import com.zippendo.sdk.api.ShipmentsApi;
import com.zippendo.sdk.api.ShipmentsApi.*;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.zippendo.com");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        ShipmentsApi apiInstance = new ShipmentsApi(defaultClient);
        String orgId = "org_1a2b3c4d"; // String | Organization identifier.
        String shipmentId = "shp_4d9e7a2f"; // String | Shipment identifier.
        try {
            APItrackShipmentRequest request = APItrackShipmentRequest.newBuilder()
                .orgId(orgId)
                .shipmentId(shipmentId)
                .build();
            ApiResponse<TrackShipment200Response> response = apiInstance.trackShipmentWithHttpInfo(request);
            System.out.println("Status code: " + response.getStatusCode());
            System.out.println("Response headers: " + response.getHeaders());
            System.out.println("Response body: " + response.getData());
        } catch (ApiException e) {
            System.err.println("Exception when calling ShipmentsApi#trackShipment");
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
| trackShipmentRequest | [**APItrackShipmentRequest**](ShipmentsApi.md#APItrackShipmentRequest)|-|-|

### Return type

ApiResponse<[**TrackShipment200Response**](TrackShipment200Response.md)>


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


<a id="APItrackShipmentRequest"></a>
## APItrackShipmentRequest
### Properties

|     Name      |    Type       | Description   |     Notes    |
| ------------- | ------------- | ------------- | -------------|
| **orgId** | **String** | Organization identifier. | |
| **shipmentId** | **String** | Shipment identifier. | |



## updateShipment

> CreateShipment201Response updateShipment(updateShipmentRequest)

Update shipment

Update an existing shipment. Only draft, pending or error shipments can be updated; an applied shipping rule overrides carrier settings and sender party.

### Example

```java
// Import classes:
import com.zippendo.sdk.ApiClient;
import com.zippendo.sdk.ApiException;
import com.zippendo.sdk.Configuration;
import com.zippendo.sdk.auth.*;
import com.zippendo.sdk.models.*;
import com.zippendo.sdk.api.ShipmentsApi;
import com.zippendo.sdk.api.ShipmentsApi.*;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.zippendo.com");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        ShipmentsApi apiInstance = new ShipmentsApi(defaultClient);
        String orgId = "org_1a2b3c4d"; // String | Organization identifier.
        String shipmentId = "shp_4d9e7a2f"; // String | Shipment identifier.
        UpdateShipmentRequest updateShipmentRequest = new UpdateShipmentRequest(); // UpdateShipmentRequest | 
        try {
            APIupdateShipmentRequest request = APIupdateShipmentRequest.newBuilder()
                .orgId(orgId)
                .shipmentId(shipmentId)
                .updateShipmentRequest(updateShipmentRequest)
                .build();
            CreateShipment201Response result = apiInstance.updateShipment(request);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling ShipmentsApi#updateShipment");
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
| updateShipmentRequest | [**APIupdateShipmentRequest**](ShipmentsApi.md#APIupdateShipmentRequest)|-|-|

### Return type

[**CreateShipment201Response**](CreateShipment201Response.md)


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

## updateShipmentWithHttpInfo

> ApiResponse<CreateShipment201Response> updateShipmentWithHttpInfo(updateShipmentRequest)

Update shipment

Update an existing shipment. Only draft, pending or error shipments can be updated; an applied shipping rule overrides carrier settings and sender party.

### Example

```java
// Import classes:
import com.zippendo.sdk.ApiClient;
import com.zippendo.sdk.ApiException;
import com.zippendo.sdk.ApiResponse;
import com.zippendo.sdk.Configuration;
import com.zippendo.sdk.auth.*;
import com.zippendo.sdk.models.*;
import com.zippendo.sdk.api.ShipmentsApi;
import com.zippendo.sdk.api.ShipmentsApi.*;

public class Example {
    public static void main(String[] args) {
        ApiClient defaultClient = Configuration.getDefaultApiClient();
        defaultClient.setBasePath("https://api.zippendo.com");
        
        // Configure HTTP bearer authorization: bearerAuth
        HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
        bearerAuth.setBearerToken("BEARER TOKEN");

        ShipmentsApi apiInstance = new ShipmentsApi(defaultClient);
        String orgId = "org_1a2b3c4d"; // String | Organization identifier.
        String shipmentId = "shp_4d9e7a2f"; // String | Shipment identifier.
        UpdateShipmentRequest updateShipmentRequest = new UpdateShipmentRequest(); // UpdateShipmentRequest | 
        try {
            APIupdateShipmentRequest request = APIupdateShipmentRequest.newBuilder()
                .orgId(orgId)
                .shipmentId(shipmentId)
                .updateShipmentRequest(updateShipmentRequest)
                .build();
            ApiResponse<CreateShipment201Response> response = apiInstance.updateShipmentWithHttpInfo(request);
            System.out.println("Status code: " + response.getStatusCode());
            System.out.println("Response headers: " + response.getHeaders());
            System.out.println("Response body: " + response.getData());
        } catch (ApiException e) {
            System.err.println("Exception when calling ShipmentsApi#updateShipment");
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
| updateShipmentRequest | [**APIupdateShipmentRequest**](ShipmentsApi.md#APIupdateShipmentRequest)|-|-|

### Return type

ApiResponse<[**CreateShipment201Response**](CreateShipment201Response.md)>


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


<a id="APIupdateShipmentRequest"></a>
## APIupdateShipmentRequest
### Properties

|     Name      |    Type       | Description   |     Notes    |
| ------------- | ------------- | ------------- | -------------|
| **orgId** | **String** | Organization identifier. | |
| **shipmentId** | **String** | Shipment identifier. | |
| **updateShipmentRequest** | [**UpdateShipmentRequest**](UpdateShipmentRequest.md) |  | |


