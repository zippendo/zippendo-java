

# ListOrderChannels200ResponseDataInner


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**id** | **String** | Unique order channel ID. |  |
|**name** | **String** | Display name of the channel. |  |
|**type** | [**TypeEnum**](#TypeEnum) | Type of the order channel (sales platform). |  |
|**enabled** | **Boolean** | Whether the channel is active. |  |
|**role** | [**RoleEnum**](#RoleEnum) | What Zippendo is used for on this channel. &#x60;orders_and_rates&#x60; (default) imports orders and serves checkout rates. &#x60;rates_only&#x60; serves checkout rates and service-point selection ONLY — orders are owned by an external system such as a WMS, nothing is imported, and no fulfillment or tracking is pushed back to the platform. |  |
|**brandId** | **String** | Brand this channel belongs to, or null for organization-wide. Orders synced from this channel inherit it, and so do the shipments and documents made from them. |  |
|**hasCredentials** | **Boolean** | Whether credentials are configured (values are never exposed). |  |
|**settings** | [**ListOrderChannels200ResponseDataInnerSettings**](ListOrderChannels200ResponseDataInnerSettings.md) |  |  |
|**webhooksEnabled** | **Boolean** | Whether real-time webhooks are enabled. |  [optional] |
|**lastSyncAt** | **OffsetDateTime** | Timestamp of the last successful sync. |  [optional] |
|**lastSyncError** | **String** | Error message from the last failed sync. |  [optional] |
|**shippingRuleIds** | **List&lt;String&gt;** | IDs of shipping rules linked to this channel. |  [optional] |
|**orgId** | **String** | Owning organization ID. |  |
|**createdAt** | **String** | Creation timestamp (ISO 8601). |  |
|**updatedAt** | **String** | Last update timestamp (ISO 8601). |  |



## Enum: TypeEnum

| Name | Value |
|---- | -----|
| SHOPIFY | &quot;shopify&quot; |
| WOOCOMMERCE | &quot;woocommerce&quot; |
| MANUAL | &quot;manual&quot; |
| CUSTOM | &quot;custom&quot; |



## Enum: RoleEnum

| Name | Value |
|---- | -----|
| ORDERS_AND_RATES | &quot;orders_and_rates&quot; |
| RATES_ONLY | &quot;rates_only&quot; |



