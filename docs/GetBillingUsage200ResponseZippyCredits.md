

# GetBillingUsage200ResponseZippyCredits

Zippy credit usage this period (present when the Zippy add-on is enabled)

## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**used** | **BigDecimal** | Zippy credits used this period, included bundle and metered alike |  |
|**included** | **BigDecimal** | Credits included in the add-on bundle this period |  |
|**billed** | **BigDecimal** | Credits beyond the bundle, metered this period |  |
|**charges** | **BigDecimal** | Metered credit charges so far, in minor units of the billing currency (whole packs) |  |
|**limit** | **BigDecimal** | Maximum Zippy credits per month (-1 for unlimited) |  |



