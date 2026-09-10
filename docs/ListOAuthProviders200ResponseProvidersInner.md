# ListOAuthProviders200ResponseProvidersInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**provider** | **str** |  | [optional] 
**provider_id** | **str** |  | [optional] 
**email** | **str** |  | [optional] 
**linked_at** | **datetime** |  | [optional] 

## Example

```python
from mudbase.models.list_o_auth_providers200_response_providers_inner import ListOAuthProviders200ResponseProvidersInner

# TODO update the JSON string below
json = "{}"
# create an instance of ListOAuthProviders200ResponseProvidersInner from a JSON string
list_o_auth_providers200_response_providers_inner_instance = ListOAuthProviders200ResponseProvidersInner.from_json(json)
# print the JSON string representation of the object
print(ListOAuthProviders200ResponseProvidersInner.to_json())

# convert the object into a dict
list_o_auth_providers200_response_providers_inner_dict = list_o_auth_providers200_response_providers_inner_instance.to_dict()
# create an instance of ListOAuthProviders200ResponseProvidersInner from a dict
list_o_auth_providers200_response_providers_inner_from_dict = ListOAuthProviders200ResponseProvidersInner.from_dict(list_o_auth_providers200_response_providers_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


