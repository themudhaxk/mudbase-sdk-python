# TriggerWebhookResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**message** | **str** |  | 
**webhook_id** | **str** | WebhookLog._id for this delivery; use in POST /api/webhooks/retry/{webhookId} | 

## Example

```python
from mudbase.models.trigger_webhook_response import TriggerWebhookResponse

# TODO update the JSON string below
json = "{}"
# create an instance of TriggerWebhookResponse from a JSON string
trigger_webhook_response_instance = TriggerWebhookResponse.from_json(json)
# print the JSON string representation of the object
print(TriggerWebhookResponse.to_json())

# convert the object into a dict
trigger_webhook_response_dict = trigger_webhook_response_instance.to_dict()
# create an instance of TriggerWebhookResponse from a dict
trigger_webhook_response_from_dict = TriggerWebhookResponse.from_dict(trigger_webhook_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


