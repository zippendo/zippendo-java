

# GetOrderChannelWebhookStatus200ResponseWebhooksInner


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**id** | **BigDecimal** | Platform webhook ID. |  |
|**topic** | **String** | Webhook event topic. |  |
|**address** | **String** | Registered callback address. |  |
|**createdAt** | **String** | Webhook creation timestamp. |  |
|**deliveryUrl** | **String** | WooCommerce delivery URL (same as &#x60;address&#x60;; present for WooCommerce channels). |  [optional] |
|**status** | **String** | WooCommerce webhook status. A value other than &#x60;active&#x60; means WooCommerce disabled the webhook (e.g. after repeated delivery failures). |  [optional] |



