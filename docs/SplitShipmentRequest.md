

# SplitShipmentRequest


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**parcelId** | **String** | Parcel whose order lines are split into a new shipment. |  |
|**orderLineIds** | **List&lt;String&gt;** | Order line IDs to move. If omitted, all order lines in the parcel are moved. |  [optional] |
|**carrierId** | **String** | Carrier for the new shipment. Copied from the original if omitted. |  [optional] |
|**productId** | **String** | Carrier product for the new shipment. Copied from the original if omitted. |  [optional] |
|**services** | **List&lt;String&gt;** | Service codes for the new shipment. Copied from the original if omitted. |  [optional] |
|**additionalParameters** | [**Map&lt;String, CreateShippingRuleRequestAdditionalParametersValue&gt;**](CreateShippingRuleRequestAdditionalParametersValue.md) | Carrier-specific parameters for the new shipment. Copied from the original if omitted. |  [optional] |
|**reference** | **String** | Reference for the new shipment. Defaults to the original reference with a suffix. |  [optional] |



