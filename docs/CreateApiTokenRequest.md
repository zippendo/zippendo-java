

# CreateApiTokenRequest


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**name** | **String** | Token name for identification |  |
|**scopes** | [**List&lt;ScopesEnum&gt;**](#List&lt;ScopesEnum&gt;) | Permission scopes for the token |  |
|**expiresInDays** | **Integer** | Token expiry in days (optional, max 365) |  [optional] |
|**brandId** | **String** | Restrict this token to a single brand. Requests made with it can only read and write that brand&#39;s data. Omit for organization-wide access. |  [optional] |



## Enum: List&lt;ScopesEnum&gt;

| Name | Value |
|---- | -----|
| READ_API_TOKENS | &quot;read:api_tokens&quot; |
| WRITE_API_TOKENS | &quot;write:api_tokens&quot; |
| READ_ORGS | &quot;read:orgs&quot; |
| WRITE_ORGS | &quot;write:orgs&quot; |
| READ_USERS | &quot;read:users&quot; |
| WRITE_USERS | &quot;write:users&quot; |
| READ_ROLES | &quot;read:roles&quot; |
| WRITE_ROLES | &quot;write:roles&quot; |
| READ_ORG_MEMBERS | &quot;read:org_members&quot; |
| WRITE_ORG_MEMBERS | &quot;write:org_members&quot; |
| READ_CARRIERS | &quot;read:carriers&quot; |
| WRITE_CARRIERS | &quot;write:carriers&quot; |
| READ_ADDRESSES | &quot;read:addresses&quot; |
| WRITE_ADDRESSES | &quot;write:addresses&quot; |
| READ_SHIPPING_RULES | &quot;read:shipping_rules&quot; |
| WRITE_SHIPPING_RULES | &quot;write:shipping_rules&quot; |
| READ_SHIPMENTS | &quot;read:shipments&quot; |
| WRITE_SHIPMENTS | &quot;write:shipments&quot; |
| READ_ORDERS | &quot;read:orders&quot; |
| WRITE_ORDERS | &quot;write:orders&quot; |
| READ_ORDER_CHANNELS | &quot;read:order_channels&quot; |
| WRITE_ORDER_CHANNELS | &quot;write:order_channels&quot; |
| READ_RETURN_PORTALS | &quot;read:return_portals&quot; |
| WRITE_RETURN_PORTALS | &quot;write:return_portals&quot; |
| READ_PRINTERS | &quot;read:printers&quot; |
| WRITE_PRINTERS | &quot;write:printers&quot; |
| READ_WEBHOOKS | &quot;read:webhooks&quot; |
| WRITE_WEBHOOKS | &quot;write:webhooks&quot; |
| READ_AUTOMATIONS | &quot;read:automations&quot; |
| WRITE_AUTOMATIONS | &quot;write:automations&quot; |
| READ_INTEGRATIONS | &quot;read:integrations&quot; |
| WRITE_INTEGRATIONS | &quot;write:integrations&quot; |
| READ_ALL | &quot;read:all&quot; |
| WRITE_ALL | &quot;write:all&quot; |



