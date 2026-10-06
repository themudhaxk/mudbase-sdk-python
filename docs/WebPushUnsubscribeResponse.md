# WebPushUnsubscribeResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**success** | **bool** |  | [optional] 
**data** | [**WebPushUnsubscribeResponseData**](WebPushUnsubscribeResponseData.md) |  | [optional] 

## Example

```python
from mudbase.models.web_push_unsubscribe_response import WebPushUnsubscribeResponse

# TODO update the JSON string below
json = "{}"
# create an instance of WebPushUnsubscribeResponse from a JSON string
web_push_unsubscribe_response_instance = WebPushUnsubscribeResponse.from_json(json)
# print the JSON string representation of the object
print(WebPushUnsubscribeResponse.to_json())

# convert the object into a dict
web_push_unsubscribe_response_dict = web_push_unsubscribe_response_instance.to_dict()
# create an instance of WebPushUnsubscribeResponse from a dict
web_push_unsubscribe_response_from_dict = WebPushUnsubscribeResponse.from_dict(web_push_unsubscribe_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


