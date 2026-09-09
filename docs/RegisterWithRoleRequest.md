# RegisterWithRoleRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**email** | **str** |  | 
**password** | **str** |  | 
**first_name** | **str** |  | 
**last_name** | **str** |  | 
**project_id** | **str** |  | 
**agreed_to_terms** | **bool** | Must be &#x60;true&#x60; - the server rejects the request otherwise. Required to stop a direct API call from creating an account without accepting the Terms of Service and Privacy Policy. | 

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


