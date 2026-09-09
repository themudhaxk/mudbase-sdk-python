# WebPushSubscribeResponseData


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**endpoint** | **str** |  | [optional] 
**user_id** | **str** |  | [optional] 
**last_seen_at** | **datetime** |  | [optional] 

## Example

```python
from mudbase.models.web_push_subscribe_response_data import WebPushSubscribeResponseData

# TODO update the JSON string below
json = "{}"
# create an instance of WebPushSubscribeResponseData from a JSON string
web_push_subscribe_response_data_instance = WebPushSubscribeResponseData.from_json(json)
# print the JSON string representation of the object
print(WebPushSubscribeResponseData.to_json())

# convert the object into a dict
web_push_subscribe_response_data_dict = web_push_subscribe_response_data_instance.to_dict()
# create an instance of WebPushSubscribeResponseData from a dict
web_push_subscribe_response_data_from_dict = WebPushSubscribeResponseData.from_dict(web_push_subscribe_response_data_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


