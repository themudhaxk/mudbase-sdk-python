# ConfigureOAuthProvider200ResponseProvider


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** |  | [optional] 
**enabled** | **bool** |  | [optional] 
**display_name** | **str** |  | [optional] 

## Example

```python
from mudbase.models.configure_o_auth_provider200_response_provider import ConfigureOAuthProvider200ResponseProvider

# TODO update the JSON string below
json = "{}"
# create an instance of ConfigureOAuthProvider200ResponseProvider from a JSON string
configure_o_auth_provider200_response_provider_instance = ConfigureOAuthProvider200ResponseProvider.from_json(json)
# print the JSON string representation of the object
print(ConfigureOAuthProvider200ResponseProvider.to_json())

# convert the object into a dict
configure_o_auth_provider200_response_provider_dict = configure_o_auth_provider200_response_provider_instance.to_dict()
# create an instance of ConfigureOAuthProvider200ResponseProvider from a dict
configure_o_auth_provider200_response_provider_from_dict = ConfigureOAuthProvider200ResponseProvider.from_dict(configure_o_auth_provider200_response_provider_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


