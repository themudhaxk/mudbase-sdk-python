# ConfigureWebhookRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**webhook_url** | **str** | URL to receive webhook payloads; set to null or omit to disable | [optional] 
**webhook_secret** | **str** | Optional secret for signing payloads (e.g. X-Webhook-Signature) | [optional] 
**webhook_events** | **List[str]** | Event types to send (e.g. collection.insert, collection.update) | [optional] 
**webhook_version** | **str** | Version string for payload format | [optional] 
**transformations** | [**List[GetWebhookConfig200ResponseDataTransformationsInner]**](GetWebhookConfig200ResponseDataTransformationsInner.md) | Transformation rules to apply to payloads before delivery | [optional] 

## Example

```python
from mudbase.models.configure_webhook_request import ConfigureWebhookRequest

# TODO update the JSON string below
json = "{}"
# create an instance of ConfigureWebhookRequest from a JSON string
configure_webhook_request_instance = ConfigureWebhookRequest.from_json(json)
# print the JSON string representation of the object
print(ConfigureWebhookRequest.to_json())

# convert the object into a dict
configure_webhook_request_dict = configure_webhook_request_instance.to_dict()
# create an instance of ConfigureWebhookRequest from a dict
configure_webhook_request_from_dict = ConfigureWebhookRequest.from_dict(configure_webhook_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


