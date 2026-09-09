# GetAvailableOAuthProviders200ResponseProvidersInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** |  | [optional] 
**display_name** | **str** |  | [optional] 
**strategy** | **str** |  | [optional] 
**default_scope** | **List[str]** |  | [optional] 
**callback_url** | **str** |  | [optional] 
**required_fields** | **List[str]** |  | [optional] 

## Example

```python
from mudbase.models.get_available_o_auth_providers200_response_providers_inner import GetAvailableOAuthProviders200ResponseProvidersInner

# TODO update the JSON string below
json = "{}"
# create an instance of GetAvailableOAuthProviders200ResponseProvidersInner from a JSON string
get_available_o_auth_providers200_response_providers_inner_instance = GetAvailableOAuthProviders200ResponseProvidersInner.from_json(json)
# print the JSON string representation of the object
print(GetAvailableOAuthProviders200ResponseProvidersInner.to_json())

# convert the object into a dict
get_available_o_auth_providers200_response_providers_inner_dict = get_available_o_auth_providers200_response_providers_inner_instance.to_dict()
# create an instance of GetAvailableOAuthProviders200ResponseProvidersInner from a dict
get_available_o_auth_providers200_response_providers_inner_from_dict = GetAvailableOAuthProviders200ResponseProvidersInner.from_dict(get_available_o_auth_providers200_response_providers_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


