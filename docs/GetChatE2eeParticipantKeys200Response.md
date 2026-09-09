# GetChatE2eeParticipantKeys200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**success** | **bool** |  | [optional] 
**data** | [**List[GetChatE2eeParticipantKeys200ResponseDataInner]**](GetChatE2eeParticipantKeys200ResponseDataInner.md) |  | [optional] 

## Example

```python
from mudbase.models.get_chat_e2ee_participant_keys200_response import GetChatE2eeParticipantKeys200Response

# TODO update the JSON string below
json = "{}"
# create an instance of GetChatE2eeParticipantKeys200Response from a JSON string
get_chat_e2ee_participant_keys200_response_instance = GetChatE2eeParticipantKeys200Response.from_json(json)
# print the JSON string representation of the object
print(GetChatE2eeParticipantKeys200Response.to_json())

# convert the object into a dict
get_chat_e2ee_participant_keys200_response_dict = get_chat_e2ee_participant_keys200_response_instance.to_dict()
# create an instance of GetChatE2eeParticipantKeys200Response from a dict
get_chat_e2ee_participant_keys200_response_from_dict = GetChatE2eeParticipantKeys200Response.from_dict(get_chat_e2ee_participant_keys200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


