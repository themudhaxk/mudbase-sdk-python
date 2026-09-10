# PushSentResponse

Result of a push send, summarized per channel. `channels.fcm` covers the device-token channel and `channels.webPush` the native Web Push channel; each is `null` when that channel had no targets in the request. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**success** | **bool** |  | [optional] 
**data** | [**PushSentResponseData**](PushSentResponseData.md) |  | [optional] 

## Example

```python
from mudbase.models.push_sent_response import PushSentResponse

# TODO update the JSON string below
json = "{}"
# create an instance of PushSentResponse from a JSON string
push_sent_response_instance = PushSentResponse.from_json(json)
# print the JSON string representation of the object
print(PushSentResponse.to_json())

# convert the object into a dict
push_sent_response_dict = push_sent_response_instance.to_dict()
# create an instance of PushSentResponse from a dict
push_sent_response_from_dict = PushSentResponse.from_dict(push_sent_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


