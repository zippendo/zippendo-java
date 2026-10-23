

# UpdateAddressRequest


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**name** | **String** | Company or person the parcel is sent from, printed on labels |  [optional] |
|**description** | **String** | Internal label for this address; send null or an empty string to clear it |  [optional] |
|**attContact** | **String** | Contact person at this address; send null or an empty string to clear it |  [optional] |
|**address1** | **String** | Address line 1 |  [optional] |
|**address2** | **String** | Address line 2; send null or an empty string to clear it |  [optional] |
|**zipcode** | **String** | Postal/ZIP code |  [optional] |
|**city** | **String** | City |  [optional] |
|**phone** | **String** | Phone number |  [optional] |
|**countryCode** | **String** | ISO country code |  [optional] |
|**state** | **String** | State/Province; send null or an empty string to clear it |  [optional] |
|**email** | **String** | Email address |  [optional] |
|**customs** | **Map&lt;String, String&gt;** | Customs identifiers |  [optional] |
|**addressTypes** | [**List&lt;AddressTypesEnum&gt;**](#List&lt;AddressTypesEnum&gt;) | Address types (sender, pickup, return) |  [optional] |
|**brandId** | **String** | Brand this record is assigned to; null (or omitted outside a brand session) keeps it organization-wide |  [optional] |



## Enum: List&lt;AddressTypesEnum&gt;

| Name | Value |
|---- | -----|
| SENDER | &quot;sender&quot; |
| PICKUP | &quot;pickup&quot; |
| RETURN | &quot;return&quot; |



