# GetAvailableOAuthProviders200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**providers** | [**List[GetAvailableOAuthProviders200ResponseProvidersInner]**](GetAvailableOAuthProviders200ResponseProvidersInner.md) |  | [optional] 
**total** | **int** |  | [optional] 

## Example

```python
from mudbase.models.get_available_o_auth_providers200_response import GetAvailableOAuthProviders200Response

# TODO update the JSON string below
json = "{}"
# create an instance of GetAvailableOAuthProviders200Response from a JSON string
get_available_o_auth_providers200_response_instance = GetAvailableOAuthProviders200Response.from_json(json)
# print the JSON string representation of the object
print(GetAvailableOAuthProviders200Response.to_json())

# convert the object into a dict
get_available_o_auth_providers200_response_dict = get_available_o_auth_providers200_response_instance.to_dict()
# create an instance of GetAvailableOAuthProviders200Response from a dict
get_available_o_auth_providers200_response_from_dict = GetAvailableOAuthProviders200Response.from_dict(get_available_o_auth_providers200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


