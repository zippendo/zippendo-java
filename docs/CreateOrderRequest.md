

# CreateOrderRequest


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**orderNumber** | **String** | Human-readable order number. |  |
|**externalId** | **String** | Identifier of the order in the source platform. |  [optional] |
|**orderChannelId** | **String** | ID of the order channel this order belongs to. |  |
|**customerName** | **String** | Customer full name. |  [optional] |
|**customerEmail** | **String** | Customer email address. |  [optional] |
|**shippingAddress** | [**CreateOrderRequestShippingAddress**](CreateOrderRequestShippingAddress.md) |  |  [optional] |
|**orderLines** | [**List&lt;CreateOrderRequestOrderLinesInner&gt;**](CreateOrderRequestOrderLinesInner.md) | Line items in the order. |  |
|**subtotalAmount** | **BigDecimal** | Order subtotal before shipping and tax. |  [optional] |
|**totalAmount** | **BigDecimal** | Order grand total. |  [optional] |
|**currency** | **String** | ISO 4217 currency code. |  [optional] |
|**notes** | **String** | Free-form internal notes. |  [optional] |
|**shippingRuleId** | **String** | Shipping rule to ship this order with. When set, a shipment is created immediately (and dispatched if the channel has autoShipOnCreate enabled). |  [optional] |
|**shippingMethodTitle** | **String** | Shipping-method title from the source checkout; matched against the order channel&#39;s shipping-method mappings to pick a shipping rule. |  [optional] |
|**externalData** | **Map&lt;String, Object&gt;** | Raw platform-specific payload for reference. |  [optional] |



