# PushSentResponseDataChannelsWebPush


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**success_count** | **int** |  | [optional] 
**failure_count** | **int** |  | [optional] 
**pruned** | **int** | Subscriptions the push service reported as gone (404/410) and that were pruned during this send.  | [optional] 

## Example

```python
from mudbase.models.push_sent_response_data_channels_web_push import PushSentResponseDataChannelsWebPush

# TODO update the JSON string below
json = "{}"
# create an instance of PushSentResponseDataChannelsWebPush from a JSON string
push_sent_response_data_channels_web_push_instance = PushSentResponseDataChannelsWebPush.from_json(json)
# print the JSON string representation of the object
print(PushSentResponseDataChannelsWebPush.to_json())

# convert the object into a dict
push_sent_response_data_channels_web_push_dict = push_sent_response_data_channels_web_push_instance.to_dict()
# create an instance of PushSentResponseDataChannelsWebPush from a dict
push_sent_response_data_channels_web_push_from_dict = PushSentResponseDataChannelsWebPush.from_dict(push_sent_response_data_channels_web_push_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


