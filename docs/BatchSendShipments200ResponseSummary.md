

# BatchSendShipments200ResponseSummary

Aggregate counts for the batch.

## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**total** | **Integer** | Number of unique shipments requested. |  |
|**sent** | **Integer** | How many were sent successfully. |  |
|**failed** | **Integer** | How many the carrier or Zippendo rejected. |  |
|**skipped** | **Integer** | How many the batch ran out of time to attempt. Submit these again. |  |



