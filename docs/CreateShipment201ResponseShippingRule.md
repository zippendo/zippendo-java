

# CreateShipment201ResponseShippingRule


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**id** | **String** | Unique shipping rule identifier. |  |
|**name** | **String** | Display name of the shipping rule. |  |
|**carrierId** | **String** | Carrier applied by the rule. |  |
|**productId** | **String** | Carrier product applied by the rule. |  |
|**services** | **List&lt;String&gt;** | Additional service codes applied by the rule. |  |
|**addressId** | **String** | Sender address applied by the rule. |  |
|**returnShippingRuleId** | **String** | Shipping rule used for return shipments. |  [optional] |
|**autoCreateReturnShipment** | **Boolean** | Whether a return shipment is created automatically. |  [optional] |
|**autoPrintLabels** | **Boolean** | Whether labels are printed automatically on send. |  [optional] |
|**autoPrintDocuments** | **Boolean** | Whether documents are printed automatically on send. |  [optional] |
|**labelPrinterId** | **String** | Printer used for labels. |  [optional] |
|**documentPrinterId** | **String** | Printer used for documents. |  [optional] |



