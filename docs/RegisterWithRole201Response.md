# RegisterWithRole201Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**message** | **str** |  | [optional] 
**require_verification** | **bool** | True when the project requires email verification before a session is issued - no token is returned in that case. | [optional] 
**token** | **str** | JWT access token. Absent when requireVerification is true. | [optional] 
**refresh_token** | **str** | JWT refresh token. Absent when requireVerification is true. | [optional] 
**expires_in** | **int** | Access token TTL in seconds. Absent when requireVerification is true. | [optional] 
**user** | [**RegisterWithRole201ResponseUser**](RegisterWithRole201ResponseUser.md) |  | [optional] 
**role** | [**RegisterWithRole201ResponseRole**](RegisterWithRole201ResponseRole.md) |  | [optional] 

## Example

```python
from mudbase.models.register_with_role201_response import RegisterWithRole201Response

# TODO update the JSON string below
json = "{}"
# create an instance of RegisterWithRole201Response from a JSON string
register_with_role201_response_instance = RegisterWithRole201Response.from_json(json)
# print the JSON string representation of the object
print(RegisterWithRole201Response.to_json())

# convert the object into a dict
register_with_role201_response_dict = register_with_role201_response_instance.to_dict()
# create an instance of RegisterWithRole201Response from a dict
register_with_role201_response_from_dict = RegisterWithRole201Response.from_dict(register_with_role201_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


