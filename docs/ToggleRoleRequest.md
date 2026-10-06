# ToggleRoleRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**is_enabled** | **bool** |  | 

## Example

```python
from mudbase.models.toggle_role_request import ToggleRoleRequest

# TODO update the JSON string below
json = "{}"
# create an instance of ToggleRoleRequest from a JSON string
toggle_role_request_instance = ToggleRoleRequest.from_json(json)
# print the JSON string representation of the object
print(ToggleRoleRequest.to_json())

# convert the object into a dict
toggle_role_request_dict = toggle_role_request_instance.to_dict()
# create an instance of ToggleRoleRequest from a dict
toggle_role_request_from_dict = ToggleRoleRequest.from_dict(toggle_role_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


