

# ListOrderChannels200ResponseDataInnerSettings

Channel settings (webhook secret and checkout token hash omitted).

## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**useWebhooks** | **Boolean** | Use webhooks for real-time order sync. |  |
|**webhookId** | **String** | External webhook identifier for management. |  [optional] |
|**webhookIds** | **List&lt;Integer&gt;** | Registered WooCommerce webhook ids. |  [optional] |
|**webhookSecretCreatedAt** | **OffsetDateTime** | When the custom channel&#39;s webhook signing secret was issued. A non-secret signal so clients can show that a secret exists; the secret itself is never returned after creation. |  [optional] |
|**siteUrl** | **URI** | WooCommerce store URL. |  [optional] |
|**autoFulfill** | **Boolean** | Push tracking back to the platform when a shipment is dispatched. Enabled by default (opt-out) — set to false to disable write-back; an unset value still syncs. |  [optional] |
|**checkoutTokenCreatedAt** | **OffsetDateTime** | When the checkout token was issued (internal; never exposed in API responses). |  [optional] |
|**autoSync** | **Boolean** | Periodically poll the channel for new orders. |  |
|**syncIntervalMinutes** | **Integer** | Polling interval in minutes (5-1440). |  |
|**autoShipOnCreate** | **Boolean** | Create a shipment automatically when an order arrives. |  |
|**defaultCarrierId** | **String** | Default carrier ID for auto-shipping. |  [optional] |
|**defaultProductId** | **String** | Default carrier product ID for auto-shipping. |  [optional] |
|**defaultAddressId** | **String** | Default sender address ID for auto-shipping. |  [optional] |
|**shippingMethodMappings** | [**List&lt;ListOrderChannels200ResponseDataInnerSettingsShippingMethodMappingsInner&gt;**](ListOrderChannels200ResponseDataInnerSettingsShippingMethodMappingsInner.md) | Map imported shipping-method titles to shipping rules, for channels without checkout rate integration. |  [optional] |
|**syncOnlyUnfulfilled** | **Boolean** | Only import orders that are not yet fulfilled. |  |
|**syncOrdersSince** | **OffsetDateTime** | Only sync orders placed at or after this timestamp. |  [optional] |
|**servicePointCount** | **Integer** | Number of service points to show at checkout (1-20). |  |



