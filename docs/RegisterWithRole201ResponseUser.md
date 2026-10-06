# RegisterWithRole201ResponseUser


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** |  | [optional] 
**email** | **str** |  | [optional] 
**first_name** | **str** |  | [optional] 
**last_name** | **str** |  | [optional] 
**role** | **str** |  | [optional] 
**custom_role** | **str** |  | [optional] 
**email_verified** | **bool** |  | [optional] 

## Example

```python
from mudbase.models.register_with_role201_response_user import RegisterWithRole201ResponseUser

# TODO update the JSON string below
json = "{}"
# create an instance of RegisterWithRole201ResponseUser from a JSON string
register_with_role201_response_user_instance = RegisterWithRole201ResponseUser.from_json(json)
# print the JSON string representation of the object
print(RegisterWithRole201ResponseUser.to_json())

# convert the object into a dict
register_with_role201_response_user_dict = register_with_role201_response_user_instance.to_dict()
# create an instance of RegisterWithRole201ResponseUser from a dict
register_with_role201_response_user_from_dict = RegisterWithRole201ResponseUser.from_dict(register_with_role201_response_user_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


