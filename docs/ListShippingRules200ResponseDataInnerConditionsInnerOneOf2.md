

# ListShippingRules200ResponseDataInnerConditionsInnerOneOf2


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**type** | [**TypeEnum**](#TypeEnum) | Condition type discriminator |  |
|**priceType** | [**PriceTypeEnum**](#PriceTypeEnum) | Whether to compare against subtotal (before discounts) or total (after discounts) |  |
|**min** | **BigDecimal** | Minimum cart value (inclusive) |  |
|**max** | **BigDecimal** | Maximum cart value (inclusive) |  |
|**shippingPrice** | **BigDecimal** | Shipping price when condition matches |  |
|**currency** | **String** | ISO 4217 currency code |  |



## Enum: TypeEnum

| Name | Value |
|---- | -----|
| PRICE_RANGE | &quot;priceRange&quot; |



## Enum: PriceTypeEnum

| Name | Value |
|---- | -----|
| SUBTOTAL | &quot;subtotal&quot; |
| TOTAL | &quot;total&quot; |



