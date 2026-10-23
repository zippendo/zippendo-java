

# GetOrder200Response


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**id** | **String** | Unique order ID. |  |
|**orderNumber** | **String** | Human-readable order number. |  |
|**externalId** | **String** | Identifier of the order in the source platform. |  [optional] |
|**customerName** | **String** | Customer full name. |  [optional] |
|**customerEmail** | **String** | Customer email address. |  [optional] |
|**shippingAddress** | [**CreateOrder201ResponseShippingAddress**](CreateOrder201ResponseShippingAddress.md) |  |  [optional] |
|**orderLines** | [**List&lt;GetOrder200ResponseOrderLinesInner&gt;**](GetOrder200ResponseOrderLinesInner.md) | Sold line items with quantity already allocated to outbound shipments. |  |
|**subtotalAmount** | **BigDecimal** | Order subtotal before shipping and tax. |  [optional] |
|**totalAmount** | **BigDecimal** | Order grand total. |  [optional] |
|**currency** | **String** | ISO 4217 currency code. |  [optional] |
|**status** | [**StatusEnum**](#StatusEnum) | Order fulfillment status derived from its shipments. |  |
|**shippingRuleId** | **String** | ID of the applied shipping rule. |  [optional] |
|**notes** | **String** | Free-form internal notes. |  [optional] |
|**externalData** | **Map&lt;String, Object&gt;** | Raw platform-specific payload for reference. |  [optional] |
|**orderChannelId** | **String** | ID of the order channel this order belongs to. |  |
|**orgId** | **String** | Owning organization ID. |  |
|**createdAt** | **String** | Creation timestamp (ISO 8601). |  |
|**updatedAt** | **String** | Last update timestamp (ISO 8601). |  |
|**orderChannel** | [**ListOrders200ResponseDataInnerOrderChannel**](ListOrders200ResponseDataInnerOrderChannel.md) |  |  |
|**shippingRule** | [**GetOrder200ResponseShippingRule**](GetOrder200ResponseShippingRule.md) |  |  [optional] |
|**shipments** | [**List&lt;GetOrder200ResponseShipmentsInner&gt;**](GetOrder200ResponseShipmentsInner.md) |  |  |



## Enum: StatusEnum

| Name | Value |
|---- | -----|
| PENDING | &quot;pending&quot; |
| PROCESSING | &quot;processing&quot; |
| PARTIALLY_FULFILLED | &quot;partially_fulfilled&quot; |
| FULFILLED | &quot;fulfilled&quot; |
| ERROR | &quot;error&quot; |
| CANCELLED | &quot;cancelled&quot; |



