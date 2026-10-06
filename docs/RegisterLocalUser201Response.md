# RegisterLocalUser201Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**message** | **str** |  | [optional] 
**require_verification** | **bool** | true when email verification is required; no token in response | [optional] 
**token** | **str** | Present only when requireEmailVerification is false | [optional] 
**refresh_token** | **str** | Present only when requireEmailVerification is false | [optional] 
**expires_in** | **int** | Present only when token is returned | [optional] 
**user** | [**RegisterLocalUser201ResponseUser**](RegisterLocalUser201ResponseUser.md) |  | [optional] 

## Example

```python
from mudbase.models.register_local_user201_response import RegisterLocalUser201Response

# TODO update the JSON string below
json = "{}"
# create an instance of RegisterLocalUser201Response from a JSON string
register_local_user201_response_instance = RegisterLocalUser201Response.from_json(json)
# print the JSON string representation of the object
print(RegisterLocalUser201Response.to_json())

# convert the object into a dict
register_local_user201_response_dict = register_local_user201_response_instance.to_dict()
# create an instance of RegisterLocalUser201Response from a dict
register_local_user201_response_from_dict = RegisterLocalUser201Response.from_dict(register_local_user201_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


