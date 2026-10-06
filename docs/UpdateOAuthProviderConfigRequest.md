# UpdateOAuthProviderConfigRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**enabled** | **bool** | Whether the OAuth provider is enabled | [optional] 
**client_id** | **str** | OAuth client ID from the provider | [optional] 
**client_secret** | **str** | OAuth client secret from the provider | [optional] 
**scope** | **List[str]** | OAuth scopes to request | [optional] 
**display_name** | **str** | Custom display name for the provider | [optional] 

## Example

```python
from mudbase.models.update_o_auth_provider_config_request import UpdateOAuthProviderConfigRequest

# TODO update the JSON string below
json = "{}"
# create an instance of UpdateOAuthProviderConfigRequest from a JSON string
update_o_auth_provider_config_request_instance = UpdateOAuthProviderConfigRequest.from_json(json)
# print the JSON string representation of the object
print(UpdateOAuthProviderConfigRequest.to_json())

# convert the object into a dict
update_o_auth_provider_config_request_dict = update_o_auth_provider_config_request_instance.to_dict()
# create an instance of UpdateOAuthProviderConfigRequest from a dict
update_o_auth_provider_config_request_from_dict = UpdateOAuthProviderConfigRequest.from_dict(update_o_auth_provider_config_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


