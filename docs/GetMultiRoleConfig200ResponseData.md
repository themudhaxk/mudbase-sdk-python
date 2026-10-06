# GetMultiRoleConfig200ResponseData


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**is_enabled** | **bool** |  | [optional] 
**default_role** | **str** |  | [optional] 
**settings** | **object** |  | [optional] 
**roles** | **List[object]** |  | [optional] 

## Example

```python
from mudbase.models.get_multi_role_config200_response_data import GetMultiRoleConfig200ResponseData

# TODO update the JSON string below
json = "{}"
# create an instance of GetMultiRoleConfig200ResponseData from a JSON string
get_multi_role_config200_response_data_instance = GetMultiRoleConfig200ResponseData.from_json(json)
# print the JSON string representation of the object
print(GetMultiRoleConfig200ResponseData.to_json())

# convert the object into a dict
get_multi_role_config200_response_data_dict = get_multi_role_config200_response_data_instance.to_dict()
# create an instance of GetMultiRoleConfig200ResponseData from a dict
get_multi_role_config200_response_data_from_dict = GetMultiRoleConfig200ResponseData.from_dict(get_multi_role_config200_response_data_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


