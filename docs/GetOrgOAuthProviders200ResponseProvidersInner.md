# GetOrgOAuthProviders200ResponseProvidersInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** |  | [optional] 
**display_name** | **str** |  | [optional] 
**strategy** | **str** |  | [optional] 
**default_scope** | **List[str]** |  | [optional] 
**auth_url** | **str** |  | [optional] 

## Example

```python
from mudbase.models.get_org_o_auth_providers200_response_providers_inner import GetOrgOAuthProviders200ResponseProvidersInner

# TODO update the JSON string below
json = "{}"
# create an instance of GetOrgOAuthProviders200ResponseProvidersInner from a JSON string
get_org_o_auth_providers200_response_providers_inner_instance = GetOrgOAuthProviders200ResponseProvidersInner.from_json(json)
# print the JSON string representation of the object
print(GetOrgOAuthProviders200ResponseProvidersInner.to_json())

# convert the object into a dict
get_org_o_auth_providers200_response_providers_inner_dict = get_org_o_auth_providers200_response_providers_inner_instance.to_dict()
# create an instance of GetOrgOAuthProviders200ResponseProvidersInner from a dict
get_org_o_auth_providers200_response_providers_inner_from_dict = GetOrgOAuthProviders200ResponseProvidersInner.from_dict(get_org_o_auth_providers200_response_providers_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


