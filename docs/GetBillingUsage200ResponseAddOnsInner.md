

# GetBillingUsage200ResponseAddOnsInner


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**type** | [**TypeEnum**](#TypeEnum) | Type of billing add-on |  |
|**quantity** | **BigDecimal** | Number of add-on units purchased |  |
|**unitPrice** | **BigDecimal** | Price per unit per month, in minor units of the billing currency |  |
|**totalPrice** | **BigDecimal** | Total price per month, in minor units of the billing currency |  |



## Enum: TypeEnum

| Name | Value |
|---- | -----|
| EXTRA_CARRIER | &quot;extra_carrier&quot; |
| EXTRA_CHANNEL | &quot;extra_channel&quot; |
| ZIPPY | &quot;zippy&quot; |



