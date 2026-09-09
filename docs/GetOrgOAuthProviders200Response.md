# GetOrgOAuthProviders200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**providers** | [**List[GetOrgOAuthProviders200ResponseProvidersInner]**](GetOrgOAuthProviders200ResponseProvidersInner.md) |  | [optional] 
**total** | **int** |  | [optional] 

## Example

```python
from mudbase.models.get_org_o_auth_providers200_response import GetOrgOAuthProviders200Response

# TODO update the JSON string below
json = "{}"
# create an instance of GetOrgOAuthProviders200Response from a JSON string
get_org_o_auth_providers200_response_instance = GetOrgOAuthProviders200Response.from_json(json)
# print the JSON string representation of the object
print(GetOrgOAuthProviders200Response.to_json())

# convert the object into a dict
get_org_o_auth_providers200_response_dict = get_org_o_auth_providers200_response_instance.to_dict()
# create an instance of GetOrgOAuthProviders200Response from a dict
get_org_o_auth_providers200_response_from_dict = GetOrgOAuthProviders200Response.from_dict(get_org_o_auth_providers200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


