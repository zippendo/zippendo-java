

# ListAvailableCarriers200ResponseInnerRequiredFieldsInner


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**name** | **String** | Human-readable label for the configuration field |  |
|**key** | **String** | Machine key used to store the field value |  |
|**type** | [**TypeEnum**](#TypeEnum) | Data type of the configuration field |  |
|**options** | [**List&lt;ListCarrierProducts200ResponseInnerAdditionalParametersInnerOptionsInner&gt;**](ListCarrierProducts200ResponseInnerAdditionalParametersInnerOptionsInner.md) | Selectable options for enum-type fields |  [optional] |
|**description** | **String** | Help text describing the field |  |
|**required** | **Boolean** | Whether the field is mandatory |  [optional] |



## Enum: TypeEnum

| Name | Value |
|---- | -----|
| STRING | &quot;string&quot; |
| NUMBER | &quot;number&quot; |
| BOOLEAN | &quot;boolean&quot; |
| ENUM | &quot;enum&quot; |
| DATE | &quot;date&quot; |
| ARRAY | &quot;array&quot; |
| OBJECT | &quot;object&quot; |



