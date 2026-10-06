# RequestRoleElevation200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**message** | **str** |  | [optional] 
**request_id** | **str** |  | [optional] 
**workflow** | **str** |  | [optional] 
**status** | **str** |  | [optional] 
**next_steps** | **List[str]** |  | [optional] 
**estimated_approval_time** | **str** |  | [optional] 

## Example

```python
from mudbase.models.request_role_elevation200_response import RequestRoleElevation200Response

# TODO update the JSON string below
json = "{}"
# create an instance of RequestRoleElevation200Response from a JSON string
request_role_elevation200_response_instance = RequestRoleElevation200Response.from_json(json)
# print the JSON string representation of the object
print(RequestRoleElevation200Response.to_json())

# convert the object into a dict
request_role_elevation200_response_dict = request_role_elevation200_response_instance.to_dict()
# create an instance of RequestRoleElevation200Response from a dict
request_role_elevation200_response_from_dict = RequestRoleElevation200Response.from_dict(request_role_elevation200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


