# GetUserOverview200ResponseFootprint


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**file_count** | **int** |  | [optional] 
**storage_used** | **int** |  | [optional] 
**session_count** | **int** |  | [optional] 
**api_key_count** | **int** |  | [optional] 
**collections_in_project** | **int** |  | [optional] 
**collections** | [**List[GetOrganizationUsers200ResponseUsersInnerProject]**](GetOrganizationUsers200ResponseUsersInnerProject.md) |  | [optional] 

## Example

```python
from mudbase.models.get_user_overview200_response_footprint import GetUserOverview200ResponseFootprint

# TODO update the JSON string below
json = "{}"
# create an instance of GetUserOverview200ResponseFootprint from a JSON string
get_user_overview200_response_footprint_instance = GetUserOverview200ResponseFootprint.from_json(json)
# print the JSON string representation of the object
print(GetUserOverview200ResponseFootprint.to_json())

# convert the object into a dict
get_user_overview200_response_footprint_dict = get_user_overview200_response_footprint_instance.to_dict()
# create an instance of GetUserOverview200ResponseFootprint from a dict
get_user_overview200_response_footprint_from_dict = GetUserOverview200ResponseFootprint.from_dict(get_user_overview200_response_footprint_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


