# ApiKeyPermission


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**resource** | **str** | Resource scope for this permission (auth, database, storage, functions, realtime, messaging) | 
**actions** | **List[str]** | Allowed actions on the resource | 

## Example

```python
from mudbase.models.api_key_permission import ApiKeyPermission

# TODO update the JSON string below
json = "{}"
# create an instance of ApiKeyPermission from a JSON string
api_key_permission_instance = ApiKeyPermission.from_json(json)
# print the JSON string representation of the object
print(ApiKeyPermission.to_json())

# convert the object into a dict
api_key_permission_dict = api_key_permission_instance.to_dict()
# create an instance of ApiKeyPermission from a dict
api_key_permission_from_dict = ApiKeyPermission.from_dict(api_key_permission_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


