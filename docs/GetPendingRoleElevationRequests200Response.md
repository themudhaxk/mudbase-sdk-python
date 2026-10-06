# GetPendingRoleElevationRequests200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**requests** | **List[object]** |  | [optional] 
**pagination** | **object** |  | [optional] 

## Example

```python
from mudbase.models.get_pending_role_elevation_requests200_response import GetPendingRoleElevationRequests200Response

# TODO update the JSON string below
json = "{}"
# create an instance of GetPendingRoleElevationRequests200Response from a JSON string
get_pending_role_elevation_requests200_response_instance = GetPendingRoleElevationRequests200Response.from_json(json)
# print the JSON string representation of the object
print(GetPendingRoleElevationRequests200Response.to_json())

# convert the object into a dict
get_pending_role_elevation_requests200_response_dict = get_pending_role_elevation_requests200_response_instance.to_dict()
# create an instance of GetPendingRoleElevationRequests200Response from a dict
get_pending_role_elevation_requests200_response_from_dict = GetPendingRoleElevationRequests200Response.from_dict(get_pending_role_elevation_requests200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


