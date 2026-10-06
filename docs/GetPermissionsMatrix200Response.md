# GetPermissionsMatrix200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**success** | **bool** |  | [optional] 
**data** | [**GetPermissionsMatrix200ResponseData**](GetPermissionsMatrix200ResponseData.md) |  | [optional] 

## Example

```python
from mudbase.models.get_permissions_matrix200_response import GetPermissionsMatrix200Response

# TODO update the JSON string below
json = "{}"
# create an instance of GetPermissionsMatrix200Response from a JSON string
get_permissions_matrix200_response_instance = GetPermissionsMatrix200Response.from_json(json)
# print the JSON string representation of the object
print(GetPermissionsMatrix200Response.to_json())

# convert the object into a dict
get_permissions_matrix200_response_dict = get_permissions_matrix200_response_instance.to_dict()
# create an instance of GetPermissionsMatrix200Response from a dict
get_permissions_matrix200_response_from_dict = GetPermissionsMatrix200Response.from_dict(get_permissions_matrix200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


