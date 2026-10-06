# RequestRoleElevationRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**role_slug** | **str** |  | 

## Example

```python
from mudbase.models.request_role_elevation_request import RequestRoleElevationRequest

# TODO update the JSON string below
json = "{}"
# create an instance of RequestRoleElevationRequest from a JSON string
request_role_elevation_request_instance = RequestRoleElevationRequest.from_json(json)
# print the JSON string representation of the object
print(RequestRoleElevationRequest.to_json())

# convert the object into a dict
request_role_elevation_request_dict = request_role_elevation_request_instance.to_dict()
# create an instance of RequestRoleElevationRequest from a dict
request_role_elevation_request_from_dict = RequestRoleElevationRequest.from_dict(request_role_elevation_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


