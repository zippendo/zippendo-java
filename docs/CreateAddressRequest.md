

# CreateAddressRequest


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**name** | **String** | Company or person the parcel is sent from, printed on labels |  |
|**description** | **String** | Internal label for this address; never printed or sent to a carrier |  [optional] |
|**attContact** | **String** | Contact person at this address, printed as the att. line |  [optional] |
|**address1** | **String** | Address line 1 |  |
|**address2** | **String** | Address line 2 |  [optional] |
|**zipcode** | **String** | Postal/ZIP code |  |
|**city** | **String** | City |  |
|**phone** | **String** | Phone number |  |
|**countryCode** | **String** | Country code (ISO 2 or 3 letter) |  |
|**state** | **String** | State/Province |  [optional] |
|**email** | **String** | Email address |  |
|**customs** | **Map&lt;String, String&gt;** | Customs identifiers (voec, eori, sprn, ioss, fda, duns) |  [optional] |
|**addressTypes** | [**List&lt;AddressTypesEnum&gt;**](#List&lt;AddressTypesEnum&gt;) | Address types (sender, pickup, return) |  [optional] |
|**brandId** | **String** | Brand this record is assigned to; null (or omitted outside a brand session) keeps it organization-wide |  [optional] |



## Enum: List&lt;AddressTypesEnum&gt;

| Name | Value |
|---- | -----|
| SENDER | &quot;sender&quot; |
| PICKUP | &quot;pickup&quot; |
| RETURN | &quot;return&quot; |



