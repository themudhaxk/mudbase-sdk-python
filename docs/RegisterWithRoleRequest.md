# RegisterWithRoleRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**email** | **str** |  | 
**password** | **str** |  | 
**first_name** | **str** |  | 
**last_name** | **str** |  | 
**project_id** | **str** |  | 
**agreed_to_terms** | **bool** | Optional. End users signing up inside a customer&#39;s app have never seen or agreed to Mudbase&#39;s own Terms of Service, so this field is not required here and is never recorded as platform ToS acceptance. A generated-app form may send it if the app has its own ToS checkbox, but Mudbase does not write it to any consent record.  | [optional] 

## Example

```python
from mudbase.models.register_with_role_request import RegisterWithRoleRequest

# TODO update the JSON string below
json = "{}"
# create an instance of RegisterWithRoleRequest from a JSON string
register_with_role_request_instance = RegisterWithRoleRequest.from_json(json)
# print the JSON string representation of the object
print(RegisterWithRoleRequest.to_json())

# convert the object into a dict
register_with_role_request_dict = register_with_role_request_instance.to_dict()
# create an instance of RegisterWithRoleRequest from a dict
register_with_role_request_from_dict = RegisterWithRoleRequest.from_dict(register_with_role_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


