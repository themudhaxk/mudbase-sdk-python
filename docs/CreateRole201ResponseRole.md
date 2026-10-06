# CreateRole201ResponseRole


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** |  | [optional] 
**name** | **str** |  | [optional] 
**slug** | **str** |  | [optional] 
**description** | **str** |  | [optional] 
**permissions** | [**List[CreateRole201ResponseRolePermissionsInner]**](CreateRole201ResponseRolePermissionsInner.md) |  | [optional] 
**hierarchy** | **float** |  | [optional] 
**is_system** | **bool** |  | [optional] 
**is_active** | **bool** |  | [optional] 

## Example

```python
from mudbase.models.create_role201_response_role import CreateRole201ResponseRole

# TODO update the JSON string below
json = "{}"
# create an instance of CreateRole201ResponseRole from a JSON string
create_role201_response_role_instance = CreateRole201ResponseRole.from_json(json)
# print the JSON string representation of the object
print(CreateRole201ResponseRole.to_json())

# convert the object into a dict
create_role201_response_role_dict = create_role201_response_role_instance.to_dict()
# create an instance of CreateRole201ResponseRole from a dict
create_role201_response_role_from_dict = CreateRole201ResponseRole.from_dict(create_role201_response_role_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


