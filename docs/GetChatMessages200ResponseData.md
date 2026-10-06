# GetChatMessages200ResponseData


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**messages** | [**List[GetChatMessages200ResponseDataMessagesInner]**](GetChatMessages200ResponseDataMessagesInner.md) |  | [optional] 
**total** | **int** |  | [optional] 

## Example

```python
from mudbase.models.get_chat_messages200_response_data import GetChatMessages200ResponseData

# TODO update the JSON string below
json = "{}"
# create an instance of GetChatMessages200ResponseData from a JSON string
get_chat_messages200_response_data_instance = GetChatMessages200ResponseData.from_json(json)
# print the JSON string representation of the object
print(GetChatMessages200ResponseData.to_json())

# convert the object into a dict
get_chat_messages200_response_data_dict = get_chat_messages200_response_data_instance.to_dict()
# create an instance of GetChatMessages200ResponseData from a dict
get_chat_messages200_response_data_from_dict = GetChatMessages200ResponseData.from_dict(get_chat_messages200_response_data_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


