# ConfigureWebhook200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**success** | **bool** |  | [optional] 
**message** | **str** |  | [optional] 
**data** | [**ConfigureWebhook200ResponseData**](ConfigureWebhook200ResponseData.md) |  | [optional] 

## Example

```python
from mudbase.models.configure_webhook200_response import ConfigureWebhook200Response

# TODO update the JSON string below
json = "{}"
# create an instance of ConfigureWebhook200Response from a JSON string
configure_webhook200_response_instance = ConfigureWebhook200Response.from_json(json)
# print the JSON string representation of the object
print(ConfigureWebhook200Response.to_json())

# convert the object into a dict
configure_webhook200_response_dict = configure_webhook200_response_instance.to_dict()
# create an instance of ConfigureWebhook200Response from a dict
configure_webhook200_response_from_dict = ConfigureWebhook200Response.from_dict(configure_webhook200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


