# WebhookLog

One **outbound delivery attempt** (Mudbase HTTP client → your `url`). **`_id`** is what the API calls **`webhookId`** in **`POST /api/webhooks/trigger`** and **`POST /api/webhooks/retry/{webhookId}`**. The string field **`webhookId`** below is an internal correlation id (e.g. `manual-<timestamp>`), not the path parameter for retry. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** | MongoDB id — use as &#x60;webhookId&#x60; path param for retry | [optional] 
**org** | **str** | Organization that owns the project | [optional] 
**project** | **str** | Project id this delivery belongs to | [optional] 
**webhook_id** | **str** | Internal correlation string (e.g. manual-173…), not the retry path id | [optional] 
**url** | **str** |  | [optional] 
**method** | **str** |  | [optional] 
**event** | **str** |  | [optional] 
**status** | **str** |  | [optional] 
**payload** | **object** | JSON body sent to your endpoint | [optional] 
**headers** | **object** | Outbound request headers (e.g. X-MUDBASE-Event, Content-Type) | [optional] 
**response** | [**WebhookLogResponse**](WebhookLogResponse.md) |  | [optional] 
**duration** | **int** | Round-trip time in milliseconds | [optional] 
**attempts** | **int** |  | [optional] 
**max_attempts** | **int** |  | [optional] 
**error** | **str** |  | [optional] 
**next_retry** | **datetime** |  | [optional] 
**created_at** | **datetime** |  | [optional] 
**updated_at** | **datetime** |  | [optional] 

## Example

```python
from mudbase.models.webhook_log import WebhookLog

# TODO update the JSON string below
json = "{}"
# create an instance of WebhookLog from a JSON string
webhook_log_instance = WebhookLog.from_json(json)
# print the JSON string representation of the object
print(WebhookLog.to_json())

# convert the object into a dict
webhook_log_dict = webhook_log_instance.to_dict()
# create an instance of WebhookLog from a dict
webhook_log_from_dict = WebhookLog.from_dict(webhook_log_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


