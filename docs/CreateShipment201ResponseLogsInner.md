

# CreateShipment201ResponseLogsInner


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**id** | **String** | Unique log entry identifier. |  |
|**direction** | [**DirectionEnum**](#DirectionEnum) | Direction of the logged request. |  |
|**request** | **Object** | Captured request payload. |  |
|**response** | **Object** | Captured response payload. |  [optional] |
|**statusCode** | **BigDecimal** | HTTP status code of the response. |  [optional] |
|**error** | **String** | Error message if the request failed. |  [optional] |
|**duration** | **BigDecimal** | Request duration in milliseconds. |  [optional] |
|**createdAt** | **String** | Timestamp when the log entry was created. |  |



## Enum: DirectionEnum

| Name | Value |
|---- | -----|
| INBOUND | &quot;inbound&quot; |
| OUTBOUND | &quot;outbound&quot; |
| CARRIER | &quot;carrier&quot; |



