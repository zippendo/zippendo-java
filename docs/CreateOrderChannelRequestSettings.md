

# CreateOrderChannelRequestSettings


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**useWebhooks** | **Boolean** | Use webhooks for real-time order sync. |  [optional] |
|**siteUrl** | **URI** | WooCommerce store URL. |  [optional] |
|**autoFulfill** | **Boolean** | Push tracking back to the platform when a shipment is dispatched. Enabled by default (opt-out) — set to false to disable write-back; an unset value still syncs. |  [optional] |
|**autoSync** | **Boolean** | Periodically poll the channel for new orders. |  [optional] |
|**syncIntervalMinutes** | **Integer** | Polling interval in minutes (5-1440). |  [optional] |
|**autoShipOnCreate** | **Boolean** | Create a shipment automatically when an order arrives. |  [optional] |
|**defaultCarrierId** | **String** | Default carrier ID for auto-shipping. |  [optional] |
|**defaultProductId** | **String** | Default carrier product ID for auto-shipping. |  [optional] |
|**defaultAddressId** | **String** | Default sender address ID for auto-shipping. |  [optional] |
|**shippingMethodMappings** | [**List&lt;CreateOrderChannelRequestSettingsShippingMethodMappingsInner&gt;**](CreateOrderChannelRequestSettingsShippingMethodMappingsInner.md) | Map imported shipping-method titles to shipping rules, for channels without checkout rate integration. |  [optional] |
|**syncOnlyUnfulfilled** | **Boolean** | Only import orders that are not yet fulfilled. |  [optional] |
|**syncOrdersSince** | **OffsetDateTime** | Only sync orders placed at or after this timestamp. |  [optional] |
|**servicePointCount** | **Integer** | Number of service points to show at checkout (1-20). |  [optional] |



