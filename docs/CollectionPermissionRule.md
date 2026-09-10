# CollectionPermissionRule

Explicit actions + row-level conditions granted on a collection

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**actions** | [**List[CollectionAction]**](CollectionAction.md) |  | [optional] 
**conditions** | **object** |  | [optional] 

## Example

```python
from mudbase.models.collection_permission_rule import CollectionPermissionRule

# TODO update the JSON string below
json = "{}"
# create an instance of CollectionPermissionRule from a JSON string
collection_permission_rule_instance = CollectionPermissionRule.from_json(json)
# print the JSON string representation of the object
print(CollectionPermissionRule.to_json())

# convert the object into a dict
collection_permission_rule_dict = collection_permission_rule_instance.to_dict()
# create an instance of CollectionPermissionRule from a dict
collection_permission_rule_from_dict = CollectionPermissionRule.from_dict(collection_permission_rule_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


