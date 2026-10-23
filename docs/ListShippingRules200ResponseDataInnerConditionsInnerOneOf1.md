

# ListShippingRules200ResponseDataInnerConditionsInnerOneOf1


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**type** | [**TypeEnum**](#TypeEnum) | Condition type discriminator |  |
|**priceType** | [**PriceTypeEnum**](#PriceTypeEnum) | Whether to compare against subtotal (before discounts) or total (after discounts) |  |
|**operator** | [**OperatorEnum**](#OperatorEnum) | Comparison operator |  |
|**value** | **BigDecimal** | Price value to compare against |  |
|**shippingPrice** | **BigDecimal** | Shipping price when condition matches |  |
|**currency** | **String** | ISO 4217 currency code |  |



## Enum: TypeEnum

| Name | Value |
|---- | -----|
| PRICE | &quot;price&quot; |



## Enum: PriceTypeEnum

| Name | Value |
|---- | -----|
| SUBTOTAL | &quot;subtotal&quot; |
| TOTAL | &quot;total&quot; |



## Enum: OperatorEnum

| Name | Value |
|---- | -----|
| GT | &quot;gt&quot; |
| GTE | &quot;gte&quot; |
| LT | &quot;lt&quot; |
| LTE | &quot;lte&quot; |
| EQ | &quot;eq&quot; |



