

# ListShippingRules200ResponseDataInnerConditionsInnerOneOf3


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**type** | [**TypeEnum**](#TypeEnum) | Condition type discriminator |  |
|**operator** | [**OperatorEnum**](#OperatorEnum) | Comparison operator |  |
|**value** | **Integer** | Quantity value to compare against |  |
|**shippingPrice** | **BigDecimal** | Shipping price when condition matches |  |
|**currency** | **String** | ISO 4217 currency code |  |



## Enum: TypeEnum

| Name | Value |
|---- | -----|
| QUANTITY | &quot;quantity&quot; |



## Enum: OperatorEnum

| Name | Value |
|---- | -----|
| GT | &quot;gt&quot; |
| GTE | &quot;gte&quot; |
| LT | &quot;lt&quot; |
| LTE | &quot;lte&quot; |
| EQ | &quot;eq&quot; |



