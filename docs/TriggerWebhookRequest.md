# TriggerWebhookRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**project_id** | **str** | Target project (must belong to your org) | 
**url** | **str** | HTTPS URL validated against SSRF rules | 
**event** | **str** | Event name (sent as X-MUDBASE-Event) | 
**payload** | **object** | JSON body POSTed to your endpoint | 
**method** | **str** |  | [optional] [default to 'POST']

## Example

```python
from mudbase.models.trigger_webhook_request import TriggerWebhookRequest

# TODO update the JSON string below
json = "{}"
# create an instance of TriggerWebhookRequest from a JSON string
trigger_webhook_request_instance = TriggerWebhookRequest.from_json(json)
# print the JSON string representation of the object
print(TriggerWebhookRequest.to_json())

# convert the object into a dict
trigger_webhook_request_dict = trigger_webhook_request_instance.to_dict()
# create an instance of TriggerWebhookRequest from a dict
trigger_webhook_request_from_dict = TriggerWebhookRequest.from_dict(trigger_webhook_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


