# GetPermissionsMatrix200ResponseData


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**collections** | **List[object]** |  | [optional] 
**roles** | **List[object]** |  | [optional] 
**features** | **List[object]** | Per-role featurePermissions for app JWT gates | [optional] 

## Example

```python
from mudbase.models.get_permissions_matrix200_response_data import GetPermissionsMatrix200ResponseData

# TODO update the JSON string below
json = "{}"
# create an instance of GetPermissionsMatrix200ResponseData from a JSON string
get_permissions_matrix200_response_data_instance = GetPermissionsMatrix200ResponseData.from_json(json)
# print the JSON string representation of the object
print(GetPermissionsMatrix200ResponseData.to_json())

# convert the object into a dict
get_permissions_matrix200_response_data_dict = get_permissions_matrix200_response_data_instance.to_dict()
# create an instance of GetPermissionsMatrix200ResponseData from a dict
get_permissions_matrix200_response_data_from_dict = GetPermissionsMatrix200ResponseData.from_dict(get_permissions_matrix200_response_data_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


