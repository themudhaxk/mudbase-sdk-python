# ConfigureOAuthProvider200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**message** | **str** |  | [optional] 
**provider** | [**ConfigureOAuthProvider200ResponseProvider**](ConfigureOAuthProvider200ResponseProvider.md) |  | [optional] 

## Example

```python
from mudbase.models.configure_o_auth_provider200_response import ConfigureOAuthProvider200Response

# TODO update the JSON string below
json = "{}"
# create an instance of ConfigureOAuthProvider200Response from a JSON string
configure_o_auth_provider200_response_instance = ConfigureOAuthProvider200Response.from_json(json)
# print the JSON string representation of the object
print(ConfigureOAuthProvider200Response.to_json())

# convert the object into a dict
configure_o_auth_provider200_response_dict = configure_o_auth_provider200_response_instance.to_dict()
# create an instance of ConfigureOAuthProvider200Response from a dict
configure_o_auth_provider200_response_from_dict = ConfigureOAuthProvider200Response.from_dict(configure_o_auth_provider200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


