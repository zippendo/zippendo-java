

# UpdateOrderChannelRequest


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**brandId** | **String** | Brand this channel belongs to; null for organization-wide |  [optional] |
|**name** | **String** | Display name for the channel. |  [optional] |
|**enabled** | **Boolean** | Whether the channel is active. |  [optional] |
|**role** | [**RoleEnum**](#RoleEnum) | What Zippendo is used for on this channel. &#x60;orders_and_rates&#x60; (default) imports orders and serves checkout rates. &#x60;rates_only&#x60; serves checkout rates and service-point selection ONLY — orders are owned by an external system such as a WMS, nothing is imported, and no fulfillment or tracking is pushed back to the platform. |  [optional] |
|**credentials** | **Map&lt;String, Object&gt;** | Type-specific platform credentials. |  [optional] |
|**settings** | [**UpdateOrderChannelRequestSettings**](UpdateOrderChannelRequestSettings.md) |  |  [optional] |
|**shippingRuleIds** | **List&lt;String&gt;** | IDs of shipping rules linked to this channel. |  [optional] |



## Enum: RoleEnum

| Name | Value |
|---- | -----|
| ORDERS_AND_RATES | &quot;orders_and_rates&quot; |
| RATES_ONLY | &quot;rates_only&quot; |



