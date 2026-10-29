

# UpdateOrgRequest


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**name** | **String** | Organization name |  [optional] |
|**slug** | **String** | Organization slug |  [optional] |
|**description** | **String** | Organization description |  [optional] |
|**currency** | [**CurrencyEnum**](#CurrencyEnum) | Billing currency (ISO 4217 code) |  [optional] |
|**vatNumber** | **String** | Company VAT/tax ID for invoices |  [optional] |
|**phone** | **String** | Billing/contact phone number |  [optional] |
|**billingEmail** | **String** | Billing email for invoices |  [optional] |
|**companyName** | **String** | Legal company name |  [optional] |
|**addressLine1** | **String** | Address line 1 |  [optional] |
|**addressLine2** | **String** | Address line 2 |  [optional] |
|**city** | **String** | City |  [optional] |
|**postalCode** | **String** | Postal code |  [optional] |
|**country** | **String** | Country (ISO 3166-1 alpha-2 code) |  [optional] |
|**customs** | **Map&lt;String, String&gt;** | Organization-wide customs identifiers (EORI, IOSS, VOEC, etc.); null clears all |  [optional] |
|**packingSlipScanCode** | [**PackingSlipScanCodeEnum**](#PackingSlipScanCodeEnum) | Code printed on packing slips that a scan turns into a print: &#x60;QR&#x60;, &#x60;BARCODE&#x60;, or &#x60;NONE&#x60; for no code. |  [optional] |



## Enum: CurrencyEnum

| Name | Value |
|---- | -----|
| DKK | &quot;DKK&quot; |
| EUR | &quot;EUR&quot; |
| USD | &quot;USD&quot; |
| GBP | &quot;GBP&quot; |
| SEK | &quot;SEK&quot; |
| NOK | &quot;NOK&quot; |



## Enum: PackingSlipScanCodeEnum

| Name | Value |
|---- | -----|
| NONE | &quot;NONE&quot; |
| QR | &quot;QR&quot; |
| BARCODE | &quot;BARCODE&quot; |



