# GetUserChats200ResponseData


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**chats** | [**List[GetUserChats200ResponseDataChatsInner]**](GetUserChats200ResponseDataChatsInner.md) |  | [optional] 
**total** | **int** |  | [optional] 

## Example

```python
from mudbase.models.get_user_chats200_response_data import GetUserChats200ResponseData

# TODO update the JSON string below
json = "{}"
# create an instance of GetUserChats200ResponseData from a JSON string
get_user_chats200_response_data_instance = GetUserChats200ResponseData.from_json(json)
# print the JSON string representation of the object
print(GetUserChats200ResponseData.to_json())

# convert the object into a dict
get_user_chats200_response_data_dict = get_user_chats200_response_data_instance.to_dict()
# create an instance of GetUserChats200ResponseData from a dict
get_user_chats200_response_data_from_dict = GetUserChats200ResponseData.from_dict(get_user_chats200_response_data_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


