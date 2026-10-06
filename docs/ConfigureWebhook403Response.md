# ConfigureWebhook403Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**success** | **bool** |  | [optional] 
**error** | **str** |  | [optional] 
**limit** | **float** |  | [optional] 

## Example

```python
from mudbase.models.configure_webhook403_response import ConfigureWebhook403Response

# TODO update the JSON string below
json = "{}"
# create an instance of ConfigureWebhook403Response from a JSON string
configure_webhook403_response_instance = ConfigureWebhook403Response.from_json(json)
# print the JSON string representation of the object
print(ConfigureWebhook403Response.to_json())

# convert the object into a dict
configure_webhook403_response_dict = configure_webhook403_response_instance.to_dict()
# create an instance of ConfigureWebhook403Response from a dict
configure_webhook403_response_from_dict = ConfigureWebhook403Response.from_dict(configure_webhook403_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


