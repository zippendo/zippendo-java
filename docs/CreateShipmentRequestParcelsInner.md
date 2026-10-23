

# CreateShipmentRequestParcelsInner


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**id** | **String** | Unique parcel identifier. |  [optional] |
|**weight** | **BigDecimal** | Parcel weight in the given weight unit. |  |
|**weightUnit** | [**WeightUnitEnum**](#WeightUnitEnum) | Unit of measurement for parcel weight. |  |
|**dimensions** | [**CreateShipmentRequestParcelsInnerDimensions**](CreateShipmentRequestParcelsInnerDimensions.md) |  |  |
|**orderLines** | [**List&lt;CreateShipmentRequestParcelsInnerOrderLinesInner&gt;**](CreateShipmentRequestParcelsInnerOrderLinesInner.md) | Order lines contained in this parcel. |  |
|**trackingNumber** | **String** | Carrier tracking number for this parcel. |  [optional] |
|**trackingUrl** | **String** | Public carrier tracking URL for this parcel. |  [optional] |
|**labelFreeCode** | **String** | Label-free drop-off code for the parcel. |  [optional] |
|**qrCodeLink** | **String** | DEPRECATED — use &#x60;qrCodeDataUri&#x60; (embeddable data URI) or &#x60;qrCodeUrl&#x60; (hosted link). Catch-all that carries whichever applies, kept populated for backwards compatibility during the migration and until it is disabled. |  [optional] |
|**qrCodeDataUri** | **String** | Embeddable &#x60;data:&#x60; URI of the QR code image for label-free drop-off — base64 image bytes you can drop straight into an &lt;img&gt;/email. Populated whenever the image bytes are available, including for carriers that host the image (it is fetched and inlined); null if the carrier published no QR code or its image could not be retrieved. |  [optional] |
|**qrCodeUrl** | **String** | Carrier-hosted URL of the QR code image for label-free drop-off, returned by carriers (e.g. Bring) that link to the image rather than embedding it. Independent of &#x60;qrCodeDataUri&#x60; — both are set when the hosted image was inlined successfully; null for carriers that only return embedded bytes. |  [optional] |



## Enum: WeightUnitEnum

| Name | Value |
|---- | -----|
| KG | &quot;kg&quot; |
| G | &quot;g&quot; |
| LB | &quot;lb&quot; |
| OZ | &quot;oz&quot; |



