

# TrackShipment200Response


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**trackingNumber** | **String** | Carrier tracking number. |  |
|**trackingUrl** | **String** | Public carrier tracking URL. |  |
|**currentStatus** | [**CurrentStatusEnum**](#CurrentStatusEnum) | Latest normalized tracking status. |  |
|**estimatedDelivery** | **String** | Estimated delivery timestamp. |  [optional] |
|**events** | [**List&lt;TrackShipment200ResponseEventsInner&gt;**](TrackShipment200ResponseEventsInner.md) | Tracking events ordered from newest to oldest. |  |



## Enum: CurrentStatusEnum

| Name | Value |
|---- | -----|
| CREATED | &quot;created&quot; |
| AWAITING_PICKUP | &quot;awaiting_pickup&quot; |
| PICKED_UP | &quot;picked_up&quot; |
| IN_TRANSIT | &quot;in_transit&quot; |
| OUT_FOR_DELIVERY | &quot;out_for_delivery&quot; |
| READY_FOR_PICKUP | &quot;ready_for_pickup&quot; |
| DELIVERED | &quot;delivered&quot; |
| RETURNED | &quot;returned&quot; |
| EXCEPTION | &quot;exception&quot; |



