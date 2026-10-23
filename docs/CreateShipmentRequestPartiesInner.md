

# CreateShipmentRequestPartiesInner


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**type** | [**TypeEnum**](#TypeEnum) | Role of the party in the shipment. |  |
|**name** | **String** | Full name or company name of the party. |  |
|**attention** | **String** | Attention contact at the party. |  [optional] |
|**address1** | **String** | Primary street address line. |  |
|**address2** | **String** | Secondary address line. |  [optional] |
|**postalCode** | **String** | Postal code of the party address. |  |
|**city** | **String** | City of the party address. |  |
|**countryCode** | **String** | ISO 3166-1 alpha-2 country code. |  |
|**email** | **String** | Email address of the party. |  [optional] |
|**phone** | **String** | Phone number of the party in E.164 format. |  [optional] |
|**attributes** | [**List&lt;CreateShipmentRequestPartiesInnerAttributesInner&gt;**](CreateShipmentRequestPartiesInnerAttributesInner.md) | Additional carrier-specific attributes for the party. |  [optional] |



## Enum: TypeEnum

| Name | Value |
|---- | -----|
| SENDER | &quot;sender&quot; |
| RECEIVER | &quot;receiver&quot; |
| PICKUP | &quot;pickup&quot; |
| BILLING | &quot;billing&quot; |
| FREIGHT_PAYER | &quot;freight_payer&quot; |
| SERVICE_POINT | &quot;service_point&quot; |
| RETURN | &quot;return&quot; |



