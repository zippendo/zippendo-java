

# ListOrderChannels200ResponseDataInnerSettingsShippingMethodMappingsInner


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**match** | **String** | Shipping-method title to match against imported orders (trimmed, case-insensitive, exact). |  |
|**shippingRuleId** | **String** | Shipping rule applied to orders whose shipping-method title matches. |  |
|**servicePointSelection** | [**ServicePointSelectionEnum**](#ServicePointSelectionEnum) | For rules whose product delivers to a service point: &#39;nearest&#39; auto-selects the closest point to the receiver&#39;s address; &#39;manual&#39; keeps the shipment in draft for manual selection. |  [optional] |



## Enum: ServicePointSelectionEnum

| Name | Value |
|---- | -----|
| NEAREST | &quot;nearest&quot; |
| MANUAL | &quot;manual&quot; |



