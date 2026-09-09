# LoginLocalUser200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**message** | **str** |  | [optional] 
**token** | **str** |  | [optional] 
**refresh_token** | **str** |  | [optional] 
**expires_in** | **int** | Access token TTL in seconds | [optional] 
**user** | [**LoginLocalUser200ResponseUser**](LoginLocalUser200ResponseUser.md) |  | [optional] 

## Example

```python
from mudbase.models.login_local_user200_response import LoginLocalUser200Response

# TODO update the JSON string below
json = "{}"
# create an instance of LoginLocalUser200Response from a JSON string
login_local_user200_response_instance = LoginLocalUser200Response.from_json(json)
# print the JSON string representation of the object
print(LoginLocalUser200Response.to_json())

# convert the object into a dict
login_local_user200_response_dict = login_local_user200_response_instance.to_dict()
# create an instance of LoginLocalUser200Response from a dict
login_local_user200_response_from_dict = LoginLocalUser200Response.from_dict(login_local_user200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


