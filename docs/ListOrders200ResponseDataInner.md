

# ListOrders200ResponseDataInner


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**id** | **String** | Unique order ID. |  |
|**orderNumber** | **String** | Human-readable order number. |  |
|**customerName** | **String** | Customer full name. |  [optional] |
|**customerEmail** | **String** | Customer email address. |  [optional] |
|**status** | [**StatusEnum**](#StatusEnum) | Order fulfillment status derived from its shipments. |  |
|**brandId** | **String** | Brand this record belongs to, or null when it is organization-wide |  |
|**subtotalAmount** | **BigDecimal** | Order subtotal before shipping and tax. |  [optional] |
|**totalAmount** | **BigDecimal** | Order grand total. |  [optional] |
|**currency** | **String** | ISO 4217 currency code. |  [optional] |
|**shipmentCount** | **Integer** | Number of shipments created for the order. |  |
|**orderChannel** | [**ListOrders200ResponseDataInnerOrderChannel**](ListOrders200ResponseDataInnerOrderChannel.md) |  |  |
|**createdAt** | **String** | Creation timestamp (ISO 8601). |  |
|**updatedAt** | **String** | Last update timestamp (ISO 8601). |  |



## Enum: StatusEnum

| Name | Value |
|---- | -----|
| PENDING | &quot;pending&quot; |
| PROCESSING | &quot;processing&quot; |
| PARTIALLY_FULFILLED | &quot;partially_fulfilled&quot; |
| FULFILLED | &quot;fulfilled&quot; |
| ERROR | &quot;error&quot; |
| CANCELLED | &quot;cancelled&quot; |



