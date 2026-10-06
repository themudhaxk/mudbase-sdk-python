# ConfigureOAuthProviderRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**enabled** | **bool** | Whether the OAuth provider is enabled | 
**client_id** | **str** | OAuth client ID from the provider | 
**client_secret** | **str** | OAuth client secret from the provider | 
**scope** | **List[str]** | OAuth scopes to request | [optional] 
**display_name** | **str** | Custom display name for the provider | [optional] 

## Example

```python
from mudbase.models.configure_o_auth_provider_request import ConfigureOAuthProviderRequest

# TODO update the JSON string below
json = "{}"
# create an instance of ConfigureOAuthProviderRequest from a JSON string
configure_o_auth_provider_request_instance = ConfigureOAuthProviderRequest.from_json(json)
# print the JSON string representation of the object
print(ConfigureOAuthProviderRequest.to_json())

# convert the object into a dict
configure_o_auth_provider_request_dict = configure_o_auth_provider_request_instance.to_dict()
# create an instance of ConfigureOAuthProviderRequest from a dict
configure_o_auth_provider_request_from_dict = ConfigureOAuthProviderRequest.from_dict(configure_o_auth_provider_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


