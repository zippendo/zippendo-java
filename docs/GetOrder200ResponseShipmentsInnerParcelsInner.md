

# GetOrder200ResponseShipmentsInnerParcelsInner


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**id** | **String** | Parcel ID. |  |
|**weight** | **BigDecimal** | Parcel weight in the given unit. |  |
|**weightUnit** | [**WeightUnitEnum**](#WeightUnitEnum) | Unit of measurement for parcel weight. |  |
|**dimensions** | [**CreateShipment201ResponseParcelsInnerDimensions**](CreateShipment201ResponseParcelsInnerDimensions.md) |  |  |
|**orderLines** | [**List&lt;GetOrder200ResponseShipmentsInnerParcelsInnerOrderLinesInner&gt;**](GetOrder200ResponseShipmentsInnerParcelsInnerOrderLinesInner.md) | Contents of this parcel. |  |



## Enum: WeightUnitEnum

| Name | Value |
|---- | -----|
| KG | &quot;kg&quot; |
| G | &quot;g&quot; |
| LB | &quot;lb&quot; |
| OZ | &quot;oz&quot; |



