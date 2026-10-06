# GetUserChats200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**success** | **bool** |  | [optional] 
**data** | [**GetUserChats200ResponseData**](GetUserChats200ResponseData.md) |  | [optional] 

## Example

```python
from mudbase.models.get_user_chats200_response import GetUserChats200Response

# TODO update the JSON string below
json = "{}"
# create an instance of GetUserChats200Response from a JSON string
get_user_chats200_response_instance = GetUserChats200Response.from_json(json)
# print the JSON string representation of the object
print(GetUserChats200Response.to_json())

# convert the object into a dict
get_user_chats200_response_dict = get_user_chats200_response_instance.to_dict()
# create an instance of GetUserChats200Response from a dict
get_user_chats200_response_from_dict = GetUserChats200Response.from_dict(get_user_chats200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


