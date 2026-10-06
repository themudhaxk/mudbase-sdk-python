# CheckPermissions200ResponsePermissions


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**system** | **List[str]** |  | [optional] 
**custom** | **List[str]** |  | [optional] 
**combined** | **List[str]** |  | [optional] 

## Example

```python
from mudbase.models.check_permissions200_response_permissions import CheckPermissions200ResponsePermissions

# TODO update the JSON string below
json = "{}"
# create an instance of CheckPermissions200ResponsePermissions from a JSON string
check_permissions200_response_permissions_instance = CheckPermissions200ResponsePermissions.from_json(json)
# print the JSON string representation of the object
print(CheckPermissions200ResponsePermissions.to_json())

# convert the object into a dict
check_permissions200_response_permissions_dict = check_permissions200_response_permissions_instance.to_dict()
# create an instance of CheckPermissions200ResponsePermissions from a dict
check_permissions200_response_permissions_from_dict = CheckPermissions200ResponsePermissions.from_dict(check_permissions200_response_permissions_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


