# GetChatDetails200ResponseData


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** |  | [optional] 
**name** | **str** |  | [optional] 
**participants** | [**List[GetChatDetails200ResponseDataParticipantsInner]**](GetChatDetails200ResponseDataParticipantsInner.md) |  | [optional] 

## Example

```python
from mudbase.models.get_chat_details200_response_data import GetChatDetails200ResponseData

# TODO update the JSON string below
json = "{}"
# create an instance of GetChatDetails200ResponseData from a JSON string
get_chat_details200_response_data_instance = GetChatDetails200ResponseData.from_json(json)
# print the JSON string representation of the object
print(GetChatDetails200ResponseData.to_json())

# convert the object into a dict
get_chat_details200_response_data_dict = get_chat_details200_response_data_instance.to_dict()
# create an instance of GetChatDetails200ResponseData from a dict
get_chat_details200_response_data_from_dict = GetChatDetails200ResponseData.from_dict(get_chat_details200_response_data_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


