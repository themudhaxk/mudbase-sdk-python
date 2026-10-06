# PushSentResponseDataChannels


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**fcm** | [**PushSentResponseDataChannelsFcm**](PushSentResponseDataChannelsFcm.md) |  | [optional] 
**web_push** | [**PushSentResponseDataChannelsWebPush**](PushSentResponseDataChannelsWebPush.md) |  | [optional] 

## Example

```python
from mudbase.models.push_sent_response_data_channels import PushSentResponseDataChannels

# TODO update the JSON string below
json = "{}"
# create an instance of PushSentResponseDataChannels from a JSON string
push_sent_response_data_channels_instance = PushSentResponseDataChannels.from_json(json)
# print the JSON string representation of the object
print(PushSentResponseDataChannels.to_json())

# convert the object into a dict
push_sent_response_data_channels_dict = push_sent_response_data_channels_instance.to_dict()
# create an instance of PushSentResponseDataChannels from a dict
push_sent_response_data_channels_from_dict = PushSentResponseDataChannels.from_dict(push_sent_response_data_channels_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


