

# ListCarrierProducts200ResponseInnerAdditionalParametersInner


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**name** | **String** | Display label for the parameter |  |
|**key** | **String** | Machine key the value is stored under |  |
|**type** | [**TypeEnum**](#TypeEnum) | Data type of the parameter |  |
|**options** | [**List&lt;ListCarrierProducts200ResponseInnerAdditionalParametersInnerOptionsInner&gt;**](ListCarrierProducts200ResponseInnerAdditionalParametersInnerOptionsInner.md) | Selectable options for enum-type parameters |  [optional] |
|**description** | **String** | Description of the parameter |  |
|**isRequired** | **Boolean** | Whether the parameter is mandatory |  |
|**requiredService** | **List&lt;String&gt;** | Service IDs for which this parameter is required |  [optional] |



## Enum: TypeEnum

| Name | Value |
|---- | -----|
| STRING | &quot;string&quot; |
| NUMBER | &quot;number&quot; |
| BOOLEAN | &quot;boolean&quot; |
| ARRAY | &quot;array&quot; |
| OBJECT | &quot;object&quot; |
| DATE | &quot;date&quot; |
| ENUM | &quot;enum&quot; |



