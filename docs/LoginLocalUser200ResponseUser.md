# LoginLocalUser200ResponseUser


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** |  | [optional] 
**email** | **str** |  | [optional] 
**first_name** | **str** |  | [optional] 
**last_name** | **str** |  | [optional] 
**role** | **str** |  | [optional] 
**email_verified** | **bool** |  | [optional] 
**two_factor_enabled** | **bool** |  | [optional] 

## Example

```python
from mudbase.models.login_local_user200_response_user import LoginLocalUser200ResponseUser

# TODO update the JSON string below
json = "{}"
# create an instance of LoginLocalUser200ResponseUser from a JSON string
login_local_user200_response_user_instance = LoginLocalUser200ResponseUser.from_json(json)
# print the JSON string representation of the object
print(LoginLocalUser200ResponseUser.to_json())

# convert the object into a dict
login_local_user200_response_user_dict = login_local_user200_response_user_instance.to_dict()
# create an instance of LoginLocalUser200ResponseUser from a dict
login_local_user200_response_user_from_dict = LoginLocalUser200ResponseUser.from_dict(login_local_user200_response_user_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


