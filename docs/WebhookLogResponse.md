# WebhookLogResponse

Last HTTP response from your server (if any)

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**status** | **int** | HTTP status code from your endpoint | [optional] 
**body** | **object** | Parsed JSON when possible; otherwise structure varies | [optional] 
**headers** | **object** |  | [optional] 

## Example

```python
from mudbase.models.webhook_log_response import WebhookLogResponse

# TODO update the JSON string below
json = "{}"
# create an instance of WebhookLogResponse from a JSON string
webhook_log_response_instance = WebhookLogResponse.from_json(json)
# print the JSON string representation of the object
print(WebhookLogResponse.to_json())

# convert the object into a dict
webhook_log_response_dict = webhook_log_response_instance.to_dict()
# create an instance of WebhookLogResponse from a dict
webhook_log_response_from_dict = WebhookLogResponse.from_dict(webhook_log_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


