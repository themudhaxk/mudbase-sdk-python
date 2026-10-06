# GetUserChats200ResponseDataChatsInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** |  | [optional] 
**name** | **str** |  | [optional] 
**type** | **str** |  | [optional] 
**last_message** | [**GetUserChats200ResponseDataChatsInnerLastMessage**](GetUserChats200ResponseDataChatsInnerLastMessage.md) |  | [optional] 
**unread_count** | **int** |  | [optional] 

## Example

```python
from mudbase.models.get_user_chats200_response_data_chats_inner import GetUserChats200ResponseDataChatsInner

# TODO update the JSON string below
json = "{}"
# create an instance of GetUserChats200ResponseDataChatsInner from a JSON string
get_user_chats200_response_data_chats_inner_instance = GetUserChats200ResponseDataChatsInner.from_json(json)
# print the JSON string representation of the object
print(GetUserChats200ResponseDataChatsInner.to_json())

# convert the object into a dict
get_user_chats200_response_data_chats_inner_dict = get_user_chats200_response_data_chats_inner_instance.to_dict()
# create an instance of GetUserChats200ResponseDataChatsInner from a dict
get_user_chats200_response_data_chats_inner_from_dict = GetUserChats200ResponseDataChatsInner.from_dict(get_user_chats200_response_data_chats_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


