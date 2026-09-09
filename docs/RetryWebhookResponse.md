# RetryWebhookResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**message** | **str** |  | 
**webhook_id** | **str** | Same log _id you passed in the path | 

## Example

```python
from mudbase.models.retry_webhook_response import RetryWebhookResponse

# TODO update the JSON string below
json = "{}"
# create an instance of RetryWebhookResponse from a JSON string
retry_webhook_response_instance = RetryWebhookResponse.from_json(json)
# print the JSON string representation of the object
print(RetryWebhookResponse.to_json())

# convert the object into a dict
retry_webhook_response_dict = retry_webhook_response_instance.to_dict()
# create an instance of RetryWebhookResponse from a dict
retry_webhook_response_from_dict = RetryWebhookResponse.from_dict(retry_webhook_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


