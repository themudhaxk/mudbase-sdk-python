# CreateRoleRequestCollectionPermissionsValue


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**actions** | [**List[CollectionAction]**](CollectionAction.md) |  | [optional] 
**conditions** | **object** |  | [optional] 

## Example

```python
from mudbase.models.create_role_request_collection_permissions_value import CreateRoleRequestCollectionPermissionsValue

# TODO update the JSON string below
json = "{}"
# create an instance of CreateRoleRequestCollectionPermissionsValue from a JSON string
create_role_request_collection_permissions_value_instance = CreateRoleRequestCollectionPermissionsValue.from_json(json)
# print the JSON string representation of the object
print(CreateRoleRequestCollectionPermissionsValue.to_json())

# convert the object into a dict
create_role_request_collection_permissions_value_dict = create_role_request_collection_permissions_value_instance.to_dict()
# create an instance of CreateRoleRequestCollectionPermissionsValue from a dict
create_role_request_collection_permissions_value_from_dict = CreateRoleRequestCollectionPermissionsValue.from_dict(create_role_request_collection_permissions_value_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


