# GetOAuthProviderConfig200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** |  | [optional] 
**enabled** | **bool** |  | [optional] 
**display_name** | **str** |  | [optional] 
**config** | [**GetOAuthProviderConfig200ResponseConfig**](GetOAuthProviderConfig200ResponseConfig.md) |  | [optional] 

## Example

```python
from mudbase.models.get_o_auth_provider_config200_response import GetOAuthProviderConfig200Response

# TODO update the JSON string below
json = "{}"
# create an instance of GetOAuthProviderConfig200Response from a JSON string
get_o_auth_provider_config200_response_instance = GetOAuthProviderConfig200Response.from_json(json)
# print the JSON string representation of the object
print(GetOAuthProviderConfig200Response.to_json())

# convert the object into a dict
get_o_auth_provider_config200_response_dict = get_o_auth_provider_config200_response_instance.to_dict()
# create an instance of GetOAuthProviderConfig200Response from a dict
get_o_auth_provider_config200_response_from_dict = GetOAuthProviderConfig200Response.from_dict(get_o_auth_provider_config200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


