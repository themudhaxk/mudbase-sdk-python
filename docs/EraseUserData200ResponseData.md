# EraseUserData200ResponseData


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**already_erased** | **bool** |  | [optional] 
**subject_id** | **str** |  | [optional] 
**anonymized** | **bool** |  | [optional] 
**sessions_revoked** | **bool** |  | [optional] 

## Example

```python
from mudbase.models.erase_user_data200_response_data import EraseUserData200ResponseData

# TODO update the JSON string below
json = "{}"
# create an instance of EraseUserData200ResponseData from a JSON string
erase_user_data200_response_data_instance = EraseUserData200ResponseData.from_json(json)
# print the JSON string representation of the object
print(EraseUserData200ResponseData.to_json())

# convert the object into a dict
erase_user_data200_response_data_dict = erase_user_data200_response_data_instance.to_dict()
# create an instance of EraseUserData200ResponseData from a dict
erase_user_data200_response_data_from_dict = EraseUserData200ResponseData.from_dict(erase_user_data200_response_data_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


