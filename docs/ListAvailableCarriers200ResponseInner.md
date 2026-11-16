

# ListAvailableCarriers200ResponseInner


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**name** | **String** | Display name of the carrier |  |
|**slug** | **String** | Unique carrier slug identifier |  |
|**group** | **String** | Carrier group or family name |  [optional] |
|**description** | **String** | Short description of the carrier |  [optional] |
|**logo** | **String** | URL to the carrier logo image |  [optional] |
|**brandColor** | **String** | Carrier brand color (hex) |  [optional] |
|**learnMoreUrl** | **URI** | URL with more information about the carrier |  [optional] |
|**requiredFields** | [**List&lt;ListAvailableCarriers200ResponseInnerRequiredFieldsInner&gt;**](ListAvailableCarriers200ResponseInnerRequiredFieldsInner.md) | Configuration fields that must be provided to connect the carrier |  [optional] |
|**optionalFields** | [**List&lt;ListAvailableCarriers200ResponseInnerRequiredFieldsInner&gt;**](ListAvailableCarriers200ResponseInnerRequiredFieldsInner.md) | Optional configuration fields for the carrier |  [optional] |
|**deprecated** | **Boolean** | Whether this integration is deprecated (still works, but discouraged) |  [optional] |
|**deprecationMessage** | **String** | Guidance shown alongside the deprecated tag (e.g. what to migrate to) |  [optional] |
|**beta** | **Boolean** | Whether this integration is newly launched and still being verified in production |  [optional] |
|**generatesCustomsDocuments** | **Boolean** | Whether the carrier produces the customs declaration (CN22/CN23) itself and returns it with the label. |  [optional] |
|**generatesCommercialInvoice** | **Boolean** | Whether the carrier produces the commercial invoice itself and returns it with the label, e.g. via electronic trade documents. |  [optional] |
|**cancelsShipments** | **Boolean** | Whether a sent shipment of this carrier can be cancelled from Zippendo. |  [optional] |
|**uncancellableProductIds** | **List&lt;String&gt;** | Products whose shipments this carrier cannot cancel, although it cancels its other products (for example locker deliveries). |  [optional] |
|**verifiesCredentials** | **Boolean** | Whether Zippendo checks the credentials with the carrier when the carrier is connected or updated. |  [optional] |



