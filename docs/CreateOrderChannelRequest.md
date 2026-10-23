

# CreateOrderChannelRequest


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**name** | **String** | Display name for the channel. |  |
|**type** | [**TypeEnum**](#TypeEnum) | Type of the order channel. Platform channels (Shopify, WooCommerce) are created via their connect flows. |  |
|**brandId** | **String** | Brand this channel belongs to; null for organization-wide |  [optional] |
|**enabled** | **Boolean** | Whether the channel is active. |  [optional] |
|**role** | [**RoleEnum**](#RoleEnum) | What Zippendo is used for on this channel. &#x60;orders_and_rates&#x60; (default) imports orders and serves checkout rates. &#x60;rates_only&#x60; serves checkout rates and service-point selection ONLY — orders are owned by an external system such as a WMS, nothing is imported, and no fulfillment or tracking is pushed back to the platform. |  [optional] |
|**settings** | [**CreateOrderChannelRequestSettings**](CreateOrderChannelRequestSettings.md) |  |  [optional] |



## Enum: TypeEnum

| Name | Value |
|---- | -----|
| MANUAL | &quot;manual&quot; |
| CUSTOM | &quot;custom&quot; |



## Enum: RoleEnum

| Name | Value |
|---- | -----|
| ORDERS_AND_RATES | &quot;orders_and_rates&quot; |
| RATES_ONLY | &quot;rates_only&quot; |



