

# UpdateOrderRequest


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**orderNumber** | **String** | Human-readable order number. |  [optional] |
|**customerName** | **String** | Customer full name. |  [optional] |
|**customerEmail** | **String** | Customer email address. |  [optional] |
|**shippingAddress** | [**CreateOrderRequestShippingAddress**](CreateOrderRequestShippingAddress.md) |  |  [optional] |
|**orderLines** | [**List&lt;CreateOrderRequestOrderLinesInner&gt;**](CreateOrderRequestOrderLinesInner.md) | Line items in the order. |  [optional] |
|**subtotalAmount** | **BigDecimal** | Order subtotal before shipping and tax. |  [optional] |
|**totalAmount** | **BigDecimal** | Order grand total. |  [optional] |
|**currency** | **String** | ISO 4217 currency code. |  [optional] |
|**notes** | **String** | Free-form internal notes. |  [optional] |
|**status** | [**StatusEnum**](#StatusEnum) | Order fulfillment status derived from its shipments. |  [optional] |
|**shippingRuleId** | **String** | ID of the shipping rule to apply. |  [optional] |
|**servicePointId** | **String** | Service point ID to apply to unsent outbound shipments. |  [optional] |



## Enum: StatusEnum

| Name | Value |
|---- | -----|
| PENDING | &quot;pending&quot; |
| PROCESSING | &quot;processing&quot; |
| PARTIALLY_FULFILLED | &quot;partially_fulfilled&quot; |
| FULFILLED | &quot;fulfilled&quot; |
| ERROR | &quot;error&quot; |
| CANCELLED | &quot;cancelled&quot; |



