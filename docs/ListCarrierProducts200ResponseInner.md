

# ListCarrierProducts200ResponseInner


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**name** | **String** | Display name of the carrier product |  |
|**productId** | **String** | Unique carrier product identifier |  |
|**type** | [**TypeEnum**](#TypeEnum) | Direction of the shipment for this product |  |
|**description** | **String** | Description of the carrier product |  [optional] |
|**availableCountries** | **List&lt;String&gt;** | Receiver countries this product delivers to |  |
|**availableSenderCountries** | **List&lt;String&gt;** | Sender countries supported by this product |  |
|**isServicePoint** | **Boolean** | Whether this product delivers to a service point |  |
|**isPickupAvailable** | **Boolean** | Whether carrier pickup is available for this product |  |
|**services** | [**List&lt;ListCarrierProducts200ResponseInnerServicesInner&gt;**](ListCarrierProducts200ResponseInnerServicesInner.md) | Additional services available for this product |  [optional] |
|**additionalParameters** | [**List&lt;ListCarrierProducts200ResponseInnerAdditionalParametersInner&gt;**](ListCarrierProducts200ResponseInnerAdditionalParametersInner.md) | Extra parameters that can or must be supplied for this product |  [optional] |
|**weightLimits** | [**ListCarrierProducts200ResponseInnerWeightLimits**](ListCarrierProducts200ResponseInnerWeightLimits.md) |  |  [optional] |



## Enum: TypeEnum

| Name | Value |
|---- | -----|
| OUTBOUND | &quot;outbound&quot; |
| INBOUND | &quot;inbound&quot; |



