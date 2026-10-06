# PushSentResponseDataChannelsFcm


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**success_count** | **int** |  | [optional] 
**failure_count** | **int** |  | [optional] 

## Example

```python
from mudbase.models.push_sent_response_data_channels_fcm import PushSentResponseDataChannelsFcm

# TODO update the JSON string below
json = "{}"
# create an instance of PushSentResponseDataChannelsFcm from a JSON string
push_sent_response_data_channels_fcm_instance = PushSentResponseDataChannelsFcm.from_json(json)
# print the JSON string representation of the object
print(PushSentResponseDataChannelsFcm.to_json())

# convert the object into a dict
push_sent_response_data_channels_fcm_dict = push_sent_response_data_channels_fcm_instance.to_dict()
# create an instance of PushSentResponseDataChannelsFcm from a dict
push_sent_response_data_channels_fcm_from_dict = PushSentResponseDataChannelsFcm.from_dict(push_sent_response_data_channels_fcm_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


