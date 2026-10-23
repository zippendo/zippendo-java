

# CreateOrgBrandRequest


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**companyName** | **String** | Legal entity name printed on this brand&#39;s documents |  [optional] |
|**vatNumber** | **String** | VAT/tax ID for this brand&#39;s shipments and documents |  [optional] |
|**customs** | **Map&lt;String, String&gt;** | Customs identifiers keyed by type |  [optional] |
|**addressLine1** | **String** | Street address line 1 |  [optional] |
|**addressLine2** | **String** | Street address line 2 |  [optional] |
|**city** | **String** | City |  [optional] |
|**postalCode** | **String** | Postal code |  [optional] |
|**country** | **String** | Country (ISO 3166-1 alpha-2) |  [optional] |
|**primaryColor** | **String** | Primary brand color — document title and table headers |  [optional] |
|**secondaryColor** | **String** | Secondary brand color — subtitle, section headings, totals accent |  [optional] |
|**name** | **String** | Brand display name |  |
|**slug** | **String** | URL-safe identifier, unique within the org. Derived from the name when omitted. |  [optional] |
|**useOrgCustoms** | **Boolean** | Whether this brand ships under the organization&#39;s fiscal identity. True (the default) declares the organization&#39;s VAT number and customs identifiers and ignores the brand&#39;s own. False makes the brand&#39;s own values the sole source — nothing falls back to the organization, so an identifier the brand has not set is not declared at all. |  [optional] |



