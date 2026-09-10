# CreateRole201ResponseRolePermissionsInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**resource** | **str** |  | [optional] 
**actions** | **List[str]** |  | [optional] 
**conditions** | **object** |  | [optional] 

## Example

```python
from mudbase.models.create_role201_response_role_permissions_inner import CreateRole201ResponseRolePermissionsInner

# TODO update the JSON string below
json = "{}"
# create an instance of CreateRole201ResponseRolePermissionsInner from a JSON string
create_role201_response_role_permissions_inner_instance = CreateRole201ResponseRolePermissionsInner.from_json(json)
# print the JSON string representation of the object
print(CreateRole201ResponseRolePermissionsInner.to_json())

# convert the object into a dict
create_role201_response_role_permissions_inner_dict = create_role201_response_role_permissions_inner_instance.to_dict()
# create an instance of CreateRole201ResponseRolePermissionsInner from a dict
create_role201_response_role_permissions_inner_from_dict = CreateRole201ResponseRolePermissionsInner.from_dict(create_role201_response_role_permissions_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


