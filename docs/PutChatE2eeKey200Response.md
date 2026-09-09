# PutChatE2eeKey200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**success** | **bool** |  | [optional] 
**data** | [**PutChatE2eeKey200ResponseData**](PutChatE2eeKey200ResponseData.md) |  | [optional] 

## Example

```python
from mudbase.models.put_chat_e2ee_key200_response import PutChatE2eeKey200Response

# TODO update the JSON string below
json = "{}"
# create an instance of PutChatE2eeKey200Response from a JSON string
put_chat_e2ee_key200_response_instance = PutChatE2eeKey200Response.from_json(json)
# print the JSON string representation of the object
print(PutChatE2eeKey200Response.to_json())

# convert the object into a dict
put_chat_e2ee_key200_response_dict = put_chat_e2ee_key200_response_instance.to_dict()
# create an instance of PutChatE2eeKey200Response from a dict
put_chat_e2ee_key200_response_from_dict = PutChatE2eeKey200Response.from_dict(put_chat_e2ee_key200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


