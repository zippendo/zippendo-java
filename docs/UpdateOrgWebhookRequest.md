

# UpdateOrgWebhookRequest


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**name** | **String** | Human-readable webhook name |  [optional] |
|**url** | **URI** | Webhook endpoint URL |  [optional] |
|**events** | [**List&lt;EventsEnum&gt;**](#List&lt;EventsEnum&gt;) | Events to subscribe to |  [optional] |
|**isActive** | **Boolean** | Whether the webhook is active |  [optional] |
|**brandId** | **String** | Brand this record is assigned to; null (or omitted outside a brand session) keeps it organization-wide |  [optional] |



## Enum: List&lt;EventsEnum&gt;

| Name | Value |
|---- | -----|
| SHIPMENT_CREATED | &quot;shipment.created&quot; |
| SHIPMENT_UPDATED | &quot;shipment.updated&quot; |
| SHIPMENT_DISPATCHED | &quot;shipment.dispatched&quot; |
| SHIPMENT_CANCELLED | &quot;shipment.cancelled&quot; |
| SHIPMENT_ERROR | &quot;shipment.error&quot; |
| ORDER_CREATED | &quot;order.created&quot; |
| ORDER_UPDATED | &quot;order.updated&quot; |
| ORDER_CANCELLED | &quot;order.cancelled&quot; |
| TRACKING_UPDATED | &quot;tracking.updated&quot; |



