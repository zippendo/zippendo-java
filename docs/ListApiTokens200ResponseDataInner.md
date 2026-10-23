

# ListApiTokens200ResponseDataInner


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**id** | **String** | Unique API token identifier |  |
|**name** | **String** | Token name for identification |  |
|**tokenPrefix** | **String** | First 12 chars of the token for identification |  |
|**scopes** | **List&lt;String&gt;** | Permission scopes granted by the token |  |
|**brandId** | **String** | Brand this token is restricted to, or null for organization-wide access |  |
|**lastUsedAt** | **String** | Timestamp the token was last used (ISO 8601), null if never used |  |
|**expiresAt** | **String** | Expiry timestamp (ISO 8601), null if it never expires |  |
|**createdAt** | **String** | Creation timestamp (ISO 8601) |  |
|**createdBy** | [**ListApiTokens200ResponseDataInnerCreatedBy**](ListApiTokens200ResponseDataInnerCreatedBy.md) |  |  |



