

# CreateShippingRule201Response


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**id** | **String** | Unique shipping rule identifier |  |
|**name** | **String** | Shipping rule name |  |
|**description** | **String** | Optional description |  |
|**translations** | [**Map&lt;String, ListShippingRules200ResponseDataInnerTranslationsValue&gt;**](ListShippingRules200ResponseDataInnerTranslationsValue.md) | Checkout name and description per language |  |
|**direction** | [**DirectionEnum**](#DirectionEnum) | Whether this rule is for outbound or inbound (return) shipments |  |
|**carrierId** | **String** | Carrier ID |  |
|**productId** | **String** | Product ID from carrier |  |
|**services** | **List&lt;String&gt;** | List of selected services |  |
|**additionalParameters** | [**Map&lt;String, ListShippingRules200ResponseDataInnerAdditionalParametersValue&gt;**](ListShippingRules200ResponseDataInnerAdditionalParametersValue.md) | Carrier-specific extra parameters, keyed by the carrier parameter &#x60;key&#x60; from the product&#39;s &#x60;additionalParameters[].key&#x60;. |  |
|**addressId** | **String** | Sender address ID |  |
|**receivingCountries** | **List&lt;String&gt;** | List of supported country codes |  |
|**emailNotification** | **Boolean** | Send an email notification to the receiver |  |
|**phoneNotification** | **Boolean** | Send an SMS notification to the receiver |  |
|**minWeight** | **BigDecimal** | Minimum required weight in kg. Orders below this are excluded from the rule. |  |
|**maxWeight** | **BigDecimal** | Maximum allowed weight in kg. Orders exceeding this are excluded from the rule. |  |
|**minOrderValue** | **BigDecimal** | Minimum required order value in currency units. Orders below this are excluded from the rule. |  |
|**maxOrderValue** | **BigDecimal** | Maximum allowed order value in currency units. Orders exceeding this are excluded from the rule. |  |
|**conditions** | [**List&lt;ListShippingRules200ResponseDataInnerConditionsInner&gt;**](ListShippingRules200ResponseDataInnerConditionsInner.md) | Rule conditions (weight/price/quantity) |  |
|**generateProformaInvoice** | **Boolean** | Generate proforma invoice for shipments |  |
|**generateCommercialInvoice** | **Boolean** | Generate commercial invoice for international shipments |  |
|**generatePackingList** | **Boolean** | Generate a packing slip with parcel and item details |  |
|**autoPrintLabels** | **Boolean** | Automatically print labels when shipment is sent |  |
|**autoPrintDocuments** | **Boolean** | Automatically print documents when shipment is sent |  |
|**labelPrinterId** | **String** | ID of the label printer |  |
|**documentPrinterId** | **String** | ID of the document printer |  |
|**returnShippingRuleId** | **String** | ID of the return shipping rule |  |
|**autoCreateReturnShipment** | **Boolean** | Automatically create and send a return shipment on dispatch |  |
|**orgId** | **String** | Owning organization ID |  |
|**brandId** | **String** | Brand this record belongs to, or null when it is organization-wide |  |
|**createdAt** | **String** | Creation timestamp (ISO 8601) |  |
|**updatedAt** | **String** | Last update timestamp (ISO 8601) |  |



## Enum: DirectionEnum

| Name | Value |
|---- | -----|
| OUTBOUND | &quot;outbound&quot; |
| INBOUND | &quot;inbound&quot; |



