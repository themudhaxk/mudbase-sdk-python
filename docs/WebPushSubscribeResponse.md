# WebPushSubscribeResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**success** | **bool** |  | [optional] 
**data** | [**WebPushSubscribeResponseData**](WebPushSubscribeResponseData.md) |  | [optional] 

## Example

```python
from mudbase.models.web_push_subscribe_response import WebPushSubscribeResponse

# TODO update the JSON string below
json = "{}"
# create an instance of WebPushSubscribeResponse from a JSON string
web_push_subscribe_response_instance = WebPushSubscribeResponse.from_json(json)
# print the JSON string representation of the object
print(WebPushSubscribeResponse.to_json())

# convert the object into a dict
web_push_subscribe_response_dict = web_push_subscribe_response_instance.to_dict()
# create an instance of WebPushSubscribeResponse from a dict
web_push_subscribe_response_from_dict = WebPushSubscribeResponse.from_dict(web_push_subscribe_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


