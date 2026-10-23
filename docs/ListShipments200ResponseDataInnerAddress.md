

# ListShipments200ResponseDataInnerAddress


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**id** | **String** | Unique address identifier |  |
|**name** | **String** | Company or person the parcel is sent from, printed on labels |  |
|**description** | **String** | Internal label for this address; never printed or sent to a carrier |  |
|**attContact** | **String** | Contact person at this address, printed as the att. line |  |
|**address1** | **String** | Address line 1 |  |
|**address2** | **String** | Address line 2 |  |
|**zipcode** | **String** | Postal/ZIP code |  |
|**city** | **String** | City |  |
|**phone** | **String** | Phone number |  |
|**countryCode** | **String** | ISO country code |  |
|**state** | **String** | State/Province |  |
|**email** | **String** | Email address |  |
|**customs** | **Map&lt;String, String&gt;** | Customs identifiers keyed by type |  [optional] |
|**addressTypes** | [**List&lt;AddressTypesEnum&gt;**](#List&lt;AddressTypesEnum&gt;) | Address types (sender, pickup, return) |  |
|**orgId** | **String** | Owning organization ID |  |
|**brandId** | **String** | Brand this record belongs to, or null when it is organization-wide |  |
|**createdAt** | **String** | Creation timestamp (ISO 8601) |  |
|**updatedAt** | **String** | Last update timestamp (ISO 8601) |  |



## Enum: List&lt;AddressTypesEnum&gt;

| Name | Value |
|---- | -----|
| SENDER | &quot;sender&quot; |
| PICKUP | &quot;pickup&quot; |
| RETURN | &quot;return&quot; |



