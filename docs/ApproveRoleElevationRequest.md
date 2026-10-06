# ApproveRoleElevationRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**approved** | **bool** |  | 
**reason** | **str** | Required if approved is false | [optional] 

## Example

```python
from mudbase.models.approve_role_elevation_request import ApproveRoleElevationRequest

# TODO update the JSON string below
json = "{}"
# create an instance of ApproveRoleElevationRequest from a JSON string
approve_role_elevation_request_instance = ApproveRoleElevationRequest.from_json(json)
# print the JSON string representation of the object
print(ApproveRoleElevationRequest.to_json())

# convert the object into a dict
approve_role_elevation_request_dict = approve_role_elevation_request_instance.to_dict()
# create an instance of ApproveRoleElevationRequest from a dict
approve_role_elevation_request_from_dict = ApproveRoleElevationRequest.from_dict(approve_role_elevation_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


