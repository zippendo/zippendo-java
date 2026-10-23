

# GetOrder200ResponseShipmentsInner


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**id** | **String** | Unique shipment identifier. |  |
|**reference** | **String** | Customer-facing shipment reference. |  |
|**status** | [**StatusEnum**](#StatusEnum) | Lifecycle status of the shipment. |  |
|**type** | [**TypeEnum**](#TypeEnum) | Direction of the shipment relative to the organization. |  |
|**tracking** | [**CreateShipment201ResponseTracking**](CreateShipment201ResponseTracking.md) |  |  [optional] |
|**carrierSettings** | [**ListShipments200ResponseDataInnerCarrierSettings**](ListShipments200ResponseDataInnerCarrierSettings.md) |  |  |
|**servicePointId** | **String** | Selected service point ID. |  [optional] |
|**createdAt** | **String** | Timestamp when the shipment was created. |  |
|**updatedAt** | **String** | Timestamp when the shipment was last updated. |  |
|**shippingRuleId** | **String** | ID of the shipping rule used for this shipment. |  [optional] |
|**documents** | [**List&lt;CreateShipment201ResponseDocumentsInner&gt;**](CreateShipment201ResponseDocumentsInner.md) | Documents (labels, customs forms) for this shipment. |  [optional] |
|**parcels** | [**List&lt;GetOrder200ResponseShipmentsInnerParcelsInner&gt;**](GetOrder200ResponseShipmentsInnerParcelsInner.md) | Compact parcels for the order&#39;s fulfillment view (no QR/label payloads). |  |



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



## Enum: TypeEnum

| Name | Value |
|---- | -----|
| OUTBOUND | &quot;outbound&quot; |
| INBOUND | &quot;inbound&quot; |



