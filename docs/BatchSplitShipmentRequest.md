

# BatchSplitShipmentRequest


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**parcelId** | **String** | Parcel whose order lines are split across new shipments. |  |
|**shipments** | [**List&lt;BatchSplitShipmentRequestShipmentsInner&gt;**](BatchSplitShipmentRequestShipmentsInner.md) | New shipments to create from the split parcel. |  |
|**carrierId** | **String** | Carrier for all new shipments. Copied from the original if omitted. |  [optional] |
|**productId** | **String** | Carrier product for all new shipments. Copied from the original if omitted. |  [optional] |
|**services** | **List&lt;String&gt;** | Service codes for all new shipments. Copied from the original if omitted. |  [optional] |
|**additionalParameters** | [**Map&lt;String, CreateShippingRuleRequestAdditionalParametersValue&gt;**](CreateShippingRuleRequestAdditionalParametersValue.md) | Carrier-specific parameters for all new shipments. Copied from the original if omitted. |  [optional] |



