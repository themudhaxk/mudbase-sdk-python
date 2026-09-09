# PutChatE2eeKey200ResponseData


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**identity_public_key** | **str** |  | [optional] 
**key_version** | **int** |  | [optional] 
**updated_at** | **datetime** |  | [optional] 

## Example

```python
from mudbase.models.put_chat_e2ee_key200_response_data import PutChatE2eeKey200ResponseData

# TODO update the JSON string below
json = "{}"
# create an instance of PutChatE2eeKey200ResponseData from a JSON string
put_chat_e2ee_key200_response_data_instance = PutChatE2eeKey200ResponseData.from_json(json)
# print the JSON string representation of the object
print(PutChatE2eeKey200ResponseData.to_json())

# convert the object into a dict
put_chat_e2ee_key200_response_data_dict = put_chat_e2ee_key200_response_data_instance.to_dict()
# create an instance of PutChatE2eeKey200ResponseData from a dict
put_chat_e2ee_key200_response_data_from_dict = PutChatE2eeKey200ResponseData.from_dict(put_chat_e2ee_key200_response_data_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


