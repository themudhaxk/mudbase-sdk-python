# AuthConfig


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**providers** | [**List[AuthProvider]**](AuthProvider.md) |  | [optional] 
**notify_on_new_sign_in** | **bool** | When true, a \&quot;new sign-in detected\&quot; email is sent to the user on each project-based sign-in (local or OAuth). Counts against the org&#39;s messaging/email plan quota. Default false. Organization-based sign-in always sends this email (no quota deduction).  | [optional] [default to False]

## Example

```python
from mudbase.models.auth_config import AuthConfig

# TODO update the JSON string below
json = "{}"
# create an instance of AuthConfig from a JSON string
auth_config_instance = AuthConfig.from_json(json)
# print the JSON string representation of the object
print(AuthConfig.to_json())

# convert the object into a dict
auth_config_dict = auth_config_instance.to_dict()
# create an instance of AuthConfig from a dict
auth_config_from_dict = AuthConfig.from_dict(auth_config_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


