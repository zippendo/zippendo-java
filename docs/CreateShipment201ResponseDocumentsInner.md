

# CreateShipment201ResponseDocumentsInner


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**id** | **String** | Unique document identifier. |  |
|**shipmentId** | **String** | Identifier of the shipment this document belongs to. |  |
|**documentType** | [**DocumentTypeEnum**](#DocumentTypeEnum) | Type of shipment document. |  |
|**format** | [**FormatEnum**](#FormatEnum) | File format of the document content. |  |
|**content** | **String** | Base64-encoded document/label content. |  |
|**size** | [**SizeEnum**](#SizeEnum) | Physical print size of the document. |  |
|**createdAt** | **String** | Timestamp when the document was created. |  |
|**updatedAt** | **String** | Timestamp when the document was last updated. |  |



## Enum: DocumentTypeEnum

| Name | Value |
|---- | -----|
| LABEL | &quot;label&quot; |
| CUSTOMS_INVOICE | &quot;customs_invoice&quot; |
| COMMERCIAL_INVOICE | &quot;commercial_invoice&quot; |
| PROFORMA_INVOICE | &quot;proforma_invoice&quot; |
| PACKING_LIST | &quot;packing_list&quot; |
| CERTIFICATE_OF_ORIGIN | &quot;certificate_of_origin&quot; |
| CN22 | &quot;cn22&quot; |
| CN23 | &quot;cn23&quot; |
| OTHER | &quot;other&quot; |



## Enum: FormatEnum

| Name | Value |
|---- | -----|
| PDF | &quot;pdf&quot; |
| PNG | &quot;png&quot; |
| JPG | &quot;jpg&quot; |
| ZPL | &quot;zpl&quot; |
| SVG | &quot;svg&quot; |



## Enum: SizeEnum

| Name | Value |
|---- | -----|
| _100_X150 | &quot;100X150&quot; |
| _100_X192 | &quot;100X192&quot; |
| A4 | &quot;A4&quot; |
| _100X100 | &quot;100x100&quot; |



