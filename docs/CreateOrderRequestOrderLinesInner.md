

# CreateOrderRequestOrderLinesInner


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**sku** | **String** | Stock keeping unit identifier. |  [optional] |
|**name** | **String** | Product name. |  |
|**quantity** | **Integer** | Quantity ordered. |  |
|**unitPrice** | **BigDecimal** | Price per unit. |  [optional] |
|**totalPrice** | **BigDecimal** | Total price for the line. |  [optional] |
|**currency** | **String** | ISO 4217 currency code. |  [optional] |
|**weight** | **BigDecimal** | Item weight in the given unit. |  [optional] |
|**weightUnit** | [**WeightUnitEnum**](#WeightUnitEnum) | Unit of the weight value. |  [optional] |
|**variantId** | **String** | Platform variant identifier. |  [optional] |
|**productId** | **String** | Platform product identifier. |  [optional] |
|**imageUrl** | **URI** | Product image URL. |  [optional] |
|**hsCode** | **String** | Harmonized System customs code (6-13 digits). |  [optional] |
|**countryOfOrigin** | **String** | ISO 3166-1 alpha-2 country of origin. |  [optional] |
|**provinceOfOrigin** | **String** | ISO 3166-2 province of origin. |  [optional] |
|**barcode** | **String** | Item barcode (EAN/UPC). |  [optional] |
|**requiresShipping** | **Boolean** | Whether the item requires shipping. |  [optional] |
|**taxable** | **Boolean** | Whether the item is taxable. |  [optional] |
|**giftCard** | **Boolean** | Whether the item is a gift card. |  [optional] |
|**vendor** | **String** | Vendor or brand name. |  [optional] |
|**id** | **String** | ID of the existing order line this entry edits. Omit to add a new line. |  [optional] |



## Enum: WeightUnitEnum

| Name | Value |
|---- | -----|
| KG | &quot;kg&quot; |
| G | &quot;g&quot; |
| LB | &quot;lb&quot; |
| OZ | &quot;oz&quot; |



