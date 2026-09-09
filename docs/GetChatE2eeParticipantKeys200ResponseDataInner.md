# GetChatE2eeParticipantKeys200ResponseDataInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**user_id** | **str** |  | [optional] 
**identity_public_key** | **str** |  | [optional] 
**key_version** | **int** |  | [optional] 
**updated_at** | **datetime** |  | [optional] 

## Example

```python
from mudbase.models.get_chat_e2ee_participant_keys200_response_data_inner import GetChatE2eeParticipantKeys200ResponseDataInner

# TODO update the JSON string below
json = "{}"
# create an instance of GetChatE2eeParticipantKeys200ResponseDataInner from a JSON string
get_chat_e2ee_participant_keys200_response_data_inner_instance = GetChatE2eeParticipantKeys200ResponseDataInner.from_json(json)
# print the JSON string representation of the object
print(GetChatE2eeParticipantKeys200ResponseDataInner.to_json())

# convert the object into a dict
get_chat_e2ee_participant_keys200_response_data_inner_dict = get_chat_e2ee_participant_keys200_response_data_inner_instance.to_dict()
# create an instance of GetChatE2eeParticipantKeys200ResponseDataInner from a dict
get_chat_e2ee_participant_keys200_response_data_inner_from_dict = GetChatE2eeParticipantKeys200ResponseDataInner.from_dict(get_chat_e2ee_participant_keys200_response_data_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


