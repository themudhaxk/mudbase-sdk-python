# CheckPermissions200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**user** | **object** |  | [optional] 
**permissions** | [**CheckPermissions200ResponsePermissions**](CheckPermissions200ResponsePermissions.md) |  | [optional] 

## Example

```python
from mudbase.models.check_permissions200_response import CheckPermissions200Response

# TODO update the JSON string below
json = "{}"
# create an instance of CheckPermissions200Response from a JSON string
check_permissions200_response_instance = CheckPermissions200Response.from_json(json)
# print the JSON string representation of the object
print(CheckPermissions200Response.to_json())

# convert the object into a dict
check_permissions200_response_dict = check_permissions200_response_instance.to_dict()
# create an instance of CheckPermissions200Response from a dict
check_permissions200_response_from_dict = CheckPermissions200Response.from_dict(check_permissions200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


