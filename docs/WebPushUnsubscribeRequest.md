# WebPushUnsubscribeRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**endpoint** | **str** | The push-service endpoint of the subscription to remove. | 

## Example

```python
from mudbase.models.web_push_unsubscribe_request import WebPushUnsubscribeRequest

# TODO update the JSON string below
json = "{}"
# create an instance of WebPushUnsubscribeRequest from a JSON string
web_push_unsubscribe_request_instance = WebPushUnsubscribeRequest.from_json(json)
# print the JSON string representation of the object
print(WebPushUnsubscribeRequest.to_json())

# convert the object into a dict
web_push_unsubscribe_request_dict = web_push_unsubscribe_request_instance.to_dict()
# create an instance of WebPushUnsubscribeRequest from a dict
web_push_unsubscribe_request_from_dict = WebPushUnsubscribeRequest.from_dict(web_push_unsubscribe_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


