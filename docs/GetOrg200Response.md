

# GetOrg200Response


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**id** | **String** | Unique organization identifier |  |
|**name** | **String** | Organization name |  |
|**slug** | **String** | Organization URL slug (unique identifier) |  |
|**description** | **String** | Organization description |  |
|**currency** | **String** | Billing currency (ISO 4217 code) |  |
|**vatNumber** | **String** | Company VAT/tax ID for invoices |  [optional] |
|**billingEmail** | **String** | Billing email for invoices |  [optional] |
|**companyName** | **String** | Legal company name |  [optional] |
|**addressLine1** | **String** | Address line 1 |  [optional] |
|**addressLine2** | **String** | Address line 2 |  [optional] |
|**city** | **String** | City |  [optional] |
|**postalCode** | **String** | Postal code |  [optional] |
|**country** | **String** | Country (ISO 3166-1 alpha-2 code) |  [optional] |
|**customs** | **Map&lt;String, String&gt;** | Customs identifiers keyed by type |  [optional] |
|**packingSlipScanCode** | [**PackingSlipScanCodeEnum**](#PackingSlipScanCodeEnum) | Code printed on packing slips that a scan turns into a print: &#x60;QR&#x60;, &#x60;BARCODE&#x60;, or &#x60;NONE&#x60; for no code. |  |
|**createdAt** | **String** | Creation timestamp (ISO 8601) |  |
|**updatedAt** | **String** | Last update timestamp (ISO 8601) |  |
|**count** | [**GetOrg200ResponseCount**](GetOrg200ResponseCount.md) |  |  |



## Enum: PackingSlipScanCodeEnum

| Name | Value |
|---- | -----|
| NONE | &quot;NONE&quot; |
| QR | &quot;QR&quot; |
| BARCODE | &quot;BARCODE&quot; |



