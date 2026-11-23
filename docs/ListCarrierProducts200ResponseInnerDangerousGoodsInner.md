

# ListCarrierProducts200ResponseInnerDangerousGoodsInner


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**kind** | [**KindEnum**](#KindEnum) | &#x60;limited_quantity&#x60;: dangerous goods packed in limited quantities (LQ). &#x60;regulated&#x60;: fully regulated dangerous goods (ADR). |  |
|**serviceId** | **String** | The service that declares these dangerous goods to the carrier. |  |
|**parameters** | [**ListCarrierProducts200ResponseInnerDangerousGoodsInnerParameters**](ListCarrierProducts200ResponseInnerDangerousGoodsInnerParameters.md) |  |  |
|**ownedParameters** | **List&lt;String&gt;** | Every additional parameter that describes the declared goods, including those &#x60;parameters&#x60; does not fill. A declaration replaces them all, so a value saved for other goods is never sent. |  [optional] |
|**singleParcel** | **Boolean** | The carrier takes this declaration on a shipment of one parcel only. |  [optional] |



## Enum: KindEnum

| Name | Value |
|---- | -----|
| LIMITED_QUANTITY | &quot;limited_quantity&quot; |
| REGULATED | &quot;regulated&quot; |



