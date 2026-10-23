

# ListShipments200ResponseDataInner


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**id** | **String** | Unique shipment identifier. |  |
|**reference** | **String** | Customer-facing shipment reference. |  |
|**type** | [**TypeEnum**](#TypeEnum) | Direction of the shipment relative to the organization. |  |
|**carrierSettings** | [**ListShipments200ResponseDataInnerCarrierSettings**](ListShipments200ResponseDataInnerCarrierSettings.md) |  |  |
|**status** | [**StatusEnum**](#StatusEnum) | Lifecycle status of the shipment. |  |
|**brandId** | **String** | Brand this record belongs to, or null when it is organization-wide |  |
|**address** | [**ListShipments200ResponseDataInnerAddress**](ListShipments200ResponseDataInnerAddress.md) |  |  [optional] |
|**createdAt** | **String** | Timestamp when the shipment was created. |  |
|**updatedAt** | **String** | Timestamp when the shipment was last updated. |  |



## Enum: TypeEnum

| Name | Value |
|---- | -----|
| OUTBOUND | &quot;outbound&quot; |
| INBOUND | &quot;inbound&quot; |



## Enum: StatusEnum

| Name | Value |
|---- | -----|
| DRAFT | &quot;draft&quot; |
| PENDING | &quot;pending&quot; |
| PROCESSING | &quot;processing&quot; |
| DISPATCHED | &quot;dispatched&quot; |
| PARTLY_DISPATCHED | &quot;partly_dispatched&quot; |
| ERROR | &quot;error&quot; |
| CANCELLED | &quot;cancelled&quot; |
| ON_HOLD | &quot;on_hold&quot; |



