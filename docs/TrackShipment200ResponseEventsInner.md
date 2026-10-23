

# TrackShipment200ResponseEventsInner


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**id** | **String** | Unique tracking event identifier. |  |
|**status** | [**StatusEnum**](#StatusEnum) | Normalized tracking status for the event. |  |
|**carrierStatus** | **String** | Raw status string reported by the carrier. |  |
|**description** | **String** | Human-readable description of the event. |  |
|**location** | **String** | Location where the event was registered. |  |
|**occurredAt** | **String** | Timestamp when the event occurred. |  |



## Enum: StatusEnum

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



