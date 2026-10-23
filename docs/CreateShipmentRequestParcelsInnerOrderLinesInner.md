

# CreateShipmentRequestParcelsInnerOrderLinesInner


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**id** | **String** | Unique order line identifier. |  [optional] |
|**orderLineId** | **String** | ID of the order line this packed line came from. Null when the item did not originate from an order line, such as a free gift or a replacement part. |  [optional] |
|**sku** | **String** | Stock keeping unit of the product. Optional — not every webshop assigns SKUs. |  [optional] |
|**quantity** | **Integer** | Number of units in this order line. |  |
|**description** | **String** | Human-readable product description. |  [optional] |
|**unitPrice** | **BigDecimal** | Price per unit in the order line currency. |  [optional] |
|**currency** | **String** | ISO 4217 currency code. |  [optional] |
|**vatPercent** | **BigDecimal** | VAT percentage applied to the unit price. |  [optional] |
|**location** | **String** | Warehouse picking location. |  [optional] |
|**countryOfOrigin** | **String** | ISO 3166-1 alpha-2 country of origin. |  [optional] |
|**hsCode** | **String** | Harmonized System customs code. |  [optional] |
|**tarrifNumber** | **String** | Deprecated misspelling of &#x60;hsCode&#x60;, kept for backwards compatibility. |  [optional] |



