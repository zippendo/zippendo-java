

# ListCarriers200ResponseDataInner


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**id** | **String** | Unique carrier identifier |  |
|**name** | **String** | Carrier display name |  |
|**carrierSlug** | **String** | Carrier slug identifier |  |
|**config** | [**Map&lt;String, ListCarriers200ResponseDataInnerConfigValue&gt;**](ListCarriers200ResponseDataInnerConfigValue.md) | Carrier configuration (required and optional fields) |  |
|**orgId** | **String** | Owning organization ID |  |
|**brandId** | **String** | Brand this record belongs to, or null when it is organization-wide |  |
|**createdAt** | **String** | Creation timestamp (ISO 8601) |  |
|**updatedAt** | **String** | Last update timestamp (ISO 8601) |  |
|**logo** | **String** | Carrier logo URL |  [optional] |
|**brandColor** | **String** | Carrier brand color (hex) |  [optional] |
|**deprecated** | **Boolean** | Whether this integration is deprecated (still works, but discouraged) |  [optional] |
|**deprecationMessage** | **String** | Guidance shown alongside the deprecated tag (e.g. what to migrate to) |  [optional] |
|**beta** | **Boolean** | Whether this integration is newly launched and still being verified in production |  [optional] |
|**generatesCustomsDocuments** | **Boolean** | Whether the carrier produces the customs declaration (CN22/CN23) itself and returns it with the label. |  [optional] |
|**generatesCommercialInvoice** | **Boolean** | Whether the carrier produces the commercial invoice itself and returns it with the label, e.g. via electronic trade documents. |  [optional] |



