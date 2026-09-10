# WebPushSubscribeRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**subscription** | [**WebPushSubscription**](WebPushSubscription.md) |  | 
**user_id** | **str** | Optional end-user id to associate with this subscription, for targeted sends. | [optional] 
**device_id** | **str** | Optional client-supplied device identifier. | [optional] 

## Example

```python
from mudbase.models.web_push_subscribe_request import WebPushSubscribeRequest

# TODO update the JSON string below
json = "{}"
# create an instance of WebPushSubscribeRequest from a JSON string
web_push_subscribe_request_instance = WebPushSubscribeRequest.from_json(json)
# print the JSON string representation of the object
print(WebPushSubscribeRequest.to_json())

# convert the object into a dict
web_push_subscribe_request_dict = web_push_subscribe_request_instance.to_dict()
# create an instance of WebPushSubscribeRequest from a dict
web_push_subscribe_request_from_dict = WebPushSubscribeRequest.from_dict(web_push_subscribe_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


