# WebPushUnsubscribeResponseData


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**removed** | **bool** | True if a matching subscription was removed; false if none was registered.  | [optional] 

## Example

```python
from mudbase.models.web_push_unsubscribe_response_data import WebPushUnsubscribeResponseData

# TODO update the JSON string below
json = "{}"
# create an instance of WebPushUnsubscribeResponseData from a JSON string
web_push_unsubscribe_response_data_instance = WebPushUnsubscribeResponseData.from_json(json)
# print the JSON string representation of the object
print(WebPushUnsubscribeResponseData.to_json())

# convert the object into a dict
web_push_unsubscribe_response_data_dict = web_push_unsubscribe_response_data_instance.to_dict()
# create an instance of WebPushUnsubscribeResponseData from a dict
web_push_unsubscribe_response_data_from_dict = WebPushUnsubscribeResponseData.from_dict(web_push_unsubscribe_response_data_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


