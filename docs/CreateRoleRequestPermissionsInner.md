# CreateRoleRequestPermissionsInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**resource** | **str** |  | [optional] 
**actions** | **List[str]** |  | [optional] 
**conditions** | **object** |  | [optional] 

## Example

```python
from mudbase.models.create_role_request_permissions_inner import CreateRoleRequestPermissionsInner

# TODO update the JSON string below
json = "{}"
# create an instance of CreateRoleRequestPermissionsInner from a JSON string
create_role_request_permissions_inner_instance = CreateRoleRequestPermissionsInner.from_json(json)
# print the JSON string representation of the object
print(CreateRoleRequestPermissionsInner.to_json())

# convert the object into a dict
create_role_request_permissions_inner_dict = create_role_request_permissions_inner_instance.to_dict()
# create an instance of CreateRoleRequestPermissionsInner from a dict
create_role_request_permissions_inner_from_dict = CreateRoleRequestPermissionsInner.from_dict(create_role_request_permissions_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


