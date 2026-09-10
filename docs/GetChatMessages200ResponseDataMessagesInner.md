# GetChatMessages200ResponseDataMessagesInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** |  | [optional] 
**content** | **str** |  | [optional] 
**sender** | [**GetChatMessages200ResponseDataMessagesInnerSender**](GetChatMessages200ResponseDataMessagesInnerSender.md) |  | [optional] 
**created_at** | **datetime** |  | [optional] 

## Example

```python
from mudbase.models.get_chat_messages200_response_data_messages_inner import GetChatMessages200ResponseDataMessagesInner

# TODO update the JSON string below
json = "{}"
# create an instance of GetChatMessages200ResponseDataMessagesInner from a JSON string
get_chat_messages200_response_data_messages_inner_instance = GetChatMessages200ResponseDataMessagesInner.from_json(json)
# print the JSON string representation of the object
print(GetChatMessages200ResponseDataMessagesInner.to_json())

# convert the object into a dict
get_chat_messages200_response_data_messages_inner_dict = get_chat_messages200_response_data_messages_inner_instance.to_dict()
# create an instance of GetChatMessages200ResponseDataMessagesInner from a dict
get_chat_messages200_response_data_messages_inner_from_dict = GetChatMessages200ResponseDataMessagesInner.from_dict(get_chat_messages200_response_data_messages_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


