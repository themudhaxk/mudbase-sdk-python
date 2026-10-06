# GetIntegrations200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**integrations** | [**List[GetIntegrations200ResponseIntegrationsInner]**](GetIntegrations200ResponseIntegrationsInner.md) |  | [optional] 

## Example

```python
from mudbase.models.get_integrations200_response import GetIntegrations200Response

# TODO update the JSON string below
json = "{}"
# create an instance of GetIntegrations200Response from a JSON string
get_integrations200_response_instance = GetIntegrations200Response.from_json(json)
# print the JSON string representation of the object
print(GetIntegrations200Response.to_json())

# convert the object into a dict
get_integrations200_response_dict = get_integrations200_response_instance.to_dict()
# create an instance of GetIntegrations200Response from a dict
get_integrations200_response_from_dict = GetIntegrations200Response.from_dict(get_integrations200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


