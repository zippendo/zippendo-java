

# UpdateShippingRuleRequest


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**name** | **String** | Shipping rule name |  [optional] |
|**description** | **String** | Optional description |  [optional] |
|**translations** | [**Map&lt;String, CreateShippingRuleRequestTranslationsValue&gt;**](CreateShippingRuleRequestTranslationsValue.md) | Checkout name and description per language; a blank field falls back to the rule&#39;s own text |  [optional] |
|**direction** | [**DirectionEnum**](#DirectionEnum) | Whether this rule is for outbound or inbound (return) shipments |  [optional] |
|**carrierId** | **String** | Carrier ID |  [optional] |
|**productId** | **String** | Product ID from carrier |  [optional] |
|**services** | **List&lt;String&gt;** | List of selected services |  [optional] |
|**additionalParameters** | [**Map&lt;String, CreateShippingRuleRequestAdditionalParametersValue&gt;**](CreateShippingRuleRequestAdditionalParametersValue.md) | Carrier-specific extra parameters, keyed by the carrier parameter &#x60;key&#x60; from the product&#39;s &#x60;additionalParameters[].key&#x60;. Omit to leave the rule&#39;s parameters unchanged. |  [optional] |
|**addressId** | **String** | Sender address ID |  [optional] |
|**receivingCountries** | **List&lt;String&gt;** | List of supported country codes |  [optional] |
|**emailNotification** | **Boolean** | Send an email notification to the receiver |  [optional] |
|**phoneNotification** | **Boolean** | Send an SMS notification to the receiver |  [optional] |
|**minWeight** | **BigDecimal** | Minimum required weight in kg |  [optional] |
|**maxWeight** | **BigDecimal** | Maximum allowed weight in kg |  [optional] |
|**minOrderValue** | **BigDecimal** | Minimum required order value in currency units |  [optional] |
|**maxOrderValue** | **BigDecimal** | Maximum allowed order value in currency units |  [optional] |
|**conditions** | [**List&lt;CreateShippingRuleRequestConditionsInner&gt;**](CreateShippingRuleRequestConditionsInner.md) | Rule conditions (weight/price/quantity) |  [optional] |
|**generateProformaInvoice** | **Boolean** | Generate proforma invoice for shipments |  [optional] |
|**generateCommercialInvoice** | **Boolean** | Generate commercial invoice for international shipments |  [optional] |
|**generatePackingList** | **Boolean** | Generate a packing slip with parcel and item details |  [optional] |
|**autoPrintLabels** | **Boolean** | Automatically print labels when shipment is sent |  [optional] |
|**autoPrintDocuments** | **Boolean** | Automatically print documents when shipment is sent |  [optional] |
|**labelPrinterId** | **String** | ID of the label printer |  [optional] |
|**documentPrinterId** | **String** | ID of the document printer |  [optional] |
|**returnShippingRuleId** | **String** | ID of the return shipping rule |  [optional] |
|**autoCreateReturnShipment** | **Boolean** | Automatically create and send a return shipment on dispatch |  [optional] |
|**brandId** | **String** | Brand this record is assigned to; null (or omitted outside a brand session) keeps it organization-wide |  [optional] |



## Enum: DirectionEnum

| Name | Value |
|---- | -----|
| OUTBOUND | &quot;outbound&quot; |
| INBOUND | &quot;inbound&quot; |



