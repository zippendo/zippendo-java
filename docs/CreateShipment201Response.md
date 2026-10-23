

# CreateShipment201Response


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**id** | **String** | Unique shipment identifier. |  |
|**reference** | **String** | Customer-facing shipment reference. |  |
|**addressId** | **String** | Sender address identifier. |  [optional] |
|**servicePointId** | **String** | Selected service point ID. |  [optional] |
|**parties** | [**List&lt;CreateShipment201ResponsePartiesInner&gt;**](CreateShipment201ResponsePartiesInner.md) | Parties involved in the shipment (sender, receiver, etc.). |  |
|**type** | [**TypeEnum**](#TypeEnum) | Direction of the shipment relative to the organization. |  |
|**carrierSettings** | [**ListShipments200ResponseDataInnerCarrierSettings**](ListShipments200ResponseDataInnerCarrierSettings.md) |  |  |
|**parcels** | [**List&lt;CreateShipment201ResponseParcelsInner&gt;**](CreateShipment201ResponseParcelsInner.md) | Parcels included in the shipment. |  |
|**pickupDetails** | [**CreateShipment201ResponsePickupDetails**](CreateShipment201ResponsePickupDetails.md) |  |  [optional] |
|**termOfTrade** | **String** | Incoterm governing the shipment. |  |
|**documents** | [**List&lt;CreateShipment201ResponseDocumentsInner&gt;**](CreateShipment201ResponseDocumentsInner.md) | Documents generated for the shipment (labels, invoices). |  [optional] |
|**errors** | [**List&lt;CreateShipment201ResponseErrorsInner&gt;**](CreateShipment201ResponseErrorsInner.md) | Carrier errors recorded for the shipment. |  |
|**tracking** | [**CreateShipment201ResponseTracking**](CreateShipment201ResponseTracking.md) |  |  [optional] |
|**status** | [**StatusEnum**](#StatusEnum) | Lifecycle status of the shipment. |  |
|**orgId** | **String** | Owning organization identifier. |  |
|**orderId** | **String** | Associated order identifier. |  [optional] |
|**shippingRuleId** | **String** | Applied shipping rule identifier. |  [optional] |
|**shippingRule** | [**CreateShipment201ResponseShippingRule**](CreateShipment201ResponseShippingRule.md) |  |  [optional] |
|**labelPrinterId** | **String** | Printer assigned for labels on this shipment. |  [optional] |
|**documentPrinterId** | **String** | Printer assigned for documents on this shipment. |  [optional] |
|**logs** | [**List&lt;CreateShipment201ResponseLogsInner&gt;**](CreateShipment201ResponseLogsInner.md) | Request/response logs captured during carrier interactions. |  |
|**activities** | [**List&lt;CreateShipment201ResponseActivitiesInner&gt;**](CreateShipment201ResponseActivitiesInner.md) | Chronological activity history of the shipment. |  |
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



