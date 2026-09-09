# ConfigureWebhook200ResponseData


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**webhook_url** | **str** |  | [optional] 
**webhook_events** | **List[str]** |  | [optional] 
**webhook_version** | **str** |  | [optional] 
**transformations** | [**List[ConfigureWebhook200ResponseDataTransformationsInner]**](ConfigureWebhook200ResponseDataTransformationsInner.md) |  | [optional] 

## Example

```python
from mudbase.models.configure_webhook200_response_data import ConfigureWebhook200ResponseData

# TODO update the JSON string below
json = "{}"
# create an instance of ConfigureWebhook200ResponseData from a JSON string
configure_webhook200_response_data_instance = ConfigureWebhook200ResponseData.from_json(json)
# print the JSON string representation of the object
print(ConfigureWebhook200ResponseData.to_json())

# convert the object into a dict
configure_webhook200_response_data_dict = configure_webhook200_response_data_instance.to_dict()
# create an instance of ConfigureWebhook200ResponseData from a dict
configure_webhook200_response_data_from_dict = ConfigureWebhook200ResponseData.from_dict(configure_webhook200_response_data_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


