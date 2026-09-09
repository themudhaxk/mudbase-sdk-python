# GetOAuthProviderConfig200ResponseConfig


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**client_id** | **str** |  | [optional] 
**scope** | **List[str]** |  | [optional] 

## Example

```python
from mudbase.models.get_o_auth_provider_config200_response_config import GetOAuthProviderConfig200ResponseConfig

# TODO update the JSON string below
json = "{}"
# create an instance of GetOAuthProviderConfig200ResponseConfig from a JSON string
get_o_auth_provider_config200_response_config_instance = GetOAuthProviderConfig200ResponseConfig.from_json(json)
# print the JSON string representation of the object
print(GetOAuthProviderConfig200ResponseConfig.to_json())

# convert the object into a dict
get_o_auth_provider_config200_response_config_dict = get_o_auth_provider_config200_response_config_instance.to_dict()
# create an instance of GetOAuthProviderConfig200ResponseConfig from a dict
get_o_auth_provider_config200_response_config_from_dict = GetOAuthProviderConfig200ResponseConfig.from_dict(get_o_auth_provider_config200_response_config_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


