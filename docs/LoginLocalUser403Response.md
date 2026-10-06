# LoginLocalUser403Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**error** | **str** |  | [optional] 
**code** | **str** |  | [optional] 
**message** | **str** |  | [optional] 

## Example

```python
from mudbase.models.login_local_user403_response import LoginLocalUser403Response

# TODO update the JSON string below
json = "{}"
# create an instance of LoginLocalUser403Response from a JSON string
login_local_user403_response_instance = LoginLocalUser403Response.from_json(json)
# print the JSON string representation of the object
print(LoginLocalUser403Response.to_json())

# convert the object into a dict
login_local_user403_response_dict = login_local_user403_response_instance.to_dict()
# create an instance of LoginLocalUser403Response from a dict
login_local_user403_response_from_dict = LoginLocalUser403Response.from_dict(login_local_user403_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


