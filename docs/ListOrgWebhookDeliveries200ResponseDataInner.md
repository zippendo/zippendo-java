

# ListOrgWebhookDeliveries200ResponseDataInner


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**id** | **String** | Delivery log ID |  |
|**webhookId** | **String** | ID of the webhook this delivery belongs to |  |
|**event** | **String** | Event type that was delivered |  |
|**payload** | **Object** | JSON payload that was sent |  |
|**statusCode** | **BigDecimal** | HTTP status code returned by the endpoint |  |
|**response** | **String** | Response body returned by the endpoint |  |
|**duration** | **BigDecimal** | Request duration in milliseconds |  |
|**success** | **Boolean** | Whether the delivery succeeded |  |
|**attempt** | **BigDecimal** | Delivery attempt number |  |
|**error** | **String** | Error message if the delivery failed |  |
|**createdAt** | **String** | Delivery timestamp (ISO 8601) |  |



