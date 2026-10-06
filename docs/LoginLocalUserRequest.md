# LoginLocalUserRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**email** | **str** |  | 
**password** | **str** |  | 
**project_id** | **str** |  | [optional] 

## Example

```python
from mudbase.models.login_local_user_request import LoginLocalUserRequest

# TODO update the JSON string below
json = "{}"
# create an instance of LoginLocalUserRequest from a JSON string
login_local_user_request_instance = LoginLocalUserRequest.from_json(json)
# print the JSON string representation of the object
print(LoginLocalUserRequest.to_json())

# convert the object into a dict
login_local_user_request_dict = login_local_user_request_instance.to_dict()
# create an instance of LoginLocalUserRequest from a dict
login_local_user_request_from_dict = LoginLocalUserRequest.from_dict(login_local_user_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


