

# ListShippingRules200ResponseDataInnerConditionsInnerOneOf


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**type** | [**TypeEnum**](#TypeEnum) | Condition type discriminator |  |
|**min** | **BigDecimal** | Minimum weight in kg (inclusive) |  |
|**max** | **BigDecimal** | Maximum weight in kg (inclusive) |  |
|**shippingPrice** | **BigDecimal** | Shipping price when condition matches |  |
|**currency** | **String** | ISO 4217 currency code |  |



## Enum: TypeEnum

| Name | Value |
|---- | -----|
| WEIGHT | &quot;weight&quot; |



