

# CreateOrderChannelWebhookSecret201Response


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**secret** | **String** | The webhook signing secret. Returned only once — store it in your system; every push to the ingest URL must carry an HMAC-SHA256 hex signature of the raw body computed with it. |  |
|**webhookUrl** | **String** | The ingest URL your system pushes signed order events to. |  |
|**createdAt** | **OffsetDateTime** | When this secret was issued (ISO 8601). |  |



