

# UpdateShipmentRequest


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**reference** | **String** | Customer-facing shipment reference. |  [optional] |
|**addressId** | **String** | Sender address identifier. |  [optional] |
|**servicePointId** | **String** | Selected service point ID. |  [optional] |
|**parties** | [**List&lt;CreateShipmentRequestPartiesInner&gt;**](CreateShipmentRequestPartiesInner.md) | Parties involved in the shipment. Optional when orderId is provided. |  [optional] |
|**type** | [**TypeEnum**](#TypeEnum) | Direction of the shipment relative to the organization. |  [optional] |
|**carrierSettings** | [**UpdateShipmentRequestCarrierSettings**](UpdateShipmentRequestCarrierSettings.md) |  |  [optional] |
|**parcels** | [**List&lt;CreateShipmentRequestParcelsInner&gt;**](CreateShipmentRequestParcelsInner.md) | Parcels to include. Optional when orderId is provided. |  [optional] |
|**pickupDetails** | [**CreateShipmentRequestPickupDetails**](CreateShipmentRequestPickupDetails.md) |  |  [optional] |
|**termOfTrade** | **String** | Incoterm governing the shipment. |  [optional] |
|**status** | [**StatusEnum**](#StatusEnum) | Lifecycle status of the shipment. |  [optional] |
|**orderId** | **String** | Order to derive parties and parcels from. |  [optional] |
|**labelPrinterId** | **String** | Printer to assign for labels. |  [optional] |
|**documentPrinterId** | **String** | Printer to assign for documents. |  [optional] |
|**shippingRuleId** | **String** | Shipping rule to apply to the shipment. Pass null to clear. |  [optional] |
|**droppoint** | [**UpdateShipmentRequestDroppoint**](UpdateShipmentRequestDroppoint.md) |  |  [optional] |



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



