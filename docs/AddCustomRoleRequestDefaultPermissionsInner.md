# AddCustomRoleRequestDefaultPermissionsInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**resource** | **str** |  | [optional] 
**actions** | **List[str]** |  | [optional] 

## Example

```python
from mudbase.models.add_custom_role_request_default_permissions_inner import AddCustomRoleRequestDefaultPermissionsInner

# TODO update the JSON string below
json = "{}"
# create an instance of AddCustomRoleRequestDefaultPermissionsInner from a JSON string
add_custom_role_request_default_permissions_inner_instance = AddCustomRoleRequestDefaultPermissionsInner.from_json(json)
# print the JSON string representation of the object
print(AddCustomRoleRequestDefaultPermissionsInner.to_json())

# convert the object into a dict
add_custom_role_request_default_permissions_inner_dict = add_custom_role_request_default_permissions_inner_instance.to_dict()
# create an instance of AddCustomRoleRequestDefaultPermissionsInner from a dict
add_custom_role_request_default_permissions_inner_from_dict = AddCustomRoleRequestDefaultPermissionsInner.from_dict(add_custom_role_request_default_permissions_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


