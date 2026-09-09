# AuthResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**message** | **str** |  | [optional] 
**token** | **str** | JWT access token (use in Authorization Bearer header) | [optional] 
**refresh_token** | **str** | JWT refresh token (use with POST /api/auth/refresh to get new token pair) | [optional] 
**expires_in** | **int** | Access token TTL in seconds (e.g. 1800 for 30 minutes) | [optional] 
**user** | [**User**](User.md) |  | [optional] 

## Example

```python
from mudbase.models.auth_response import AuthResponse

# TODO update the JSON string below
json = "{}"
# create an instance of AuthResponse from a JSON string
auth_response_instance = AuthResponse.from_json(json)
# print the JSON string representation of the object
print(AuthResponse.to_json())

# convert the object into a dict
auth_response_dict = auth_response_instance.to_dict()
# create an instance of AuthResponse from a dict
auth_response_from_dict = AuthResponse.from_dict(auth_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


