

# CreateShipment201ResponseActivitiesInner


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**id** | **String** | Unique activity identifier. |  |
|**action** | [**ActionEnum**](#ActionEnum) | Type of activity performed on the shipment. |  |
|**description** | **String** | Human-readable description of the activity. |  |
|**metadata** | **Object** | Additional structured data about the activity. |  [optional] |
|**createdAt** | **String** | Timestamp when the activity occurred. |  |



## Enum: ActionEnum

| Name | Value |
|---- | -----|
| CREATED | &quot;created&quot; |
| UPDATED | &quot;updated&quot; |
| SENT | &quot;sent&quot; |
| SEND_FAILED | &quot;send_failed&quot; |
| DELETED | &quot;deleted&quot; |
| SHIPPING_RULE_APPLIED | &quot;shipping_rule_applied&quot; |
| PARCEL_SPLIT | &quot;parcel_split&quot; |
| SHIPMENT_SPLIT | &quot;shipment_split&quot; |
| RETURN_CREATED | &quot;return_created&quot; |



