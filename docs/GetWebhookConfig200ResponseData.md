# GetWebhookConfig200ResponseData


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**webhook_url** | **str** |  | [optional] 
**webhook_events** | **List[str]** |  | [optional] 
**webhook_version** | **str** |  | [optional] 
**transformations** | [**List[GetWebhookConfig200ResponseDataTransformationsInner]**](GetWebhookConfig200ResponseDataTransformationsInner.md) | Transformation rules applied to payloads | [optional] 
**has_secret** | **bool** | Whether a webhook secret is configured (value not returned) | [optional] 

## Example

```python
from mudbase.models.get_webhook_config200_response_data import GetWebhookConfig200ResponseData

# TODO update the JSON string below
json = "{}"
# create an instance of GetWebhookConfig200ResponseData from a JSON string
get_webhook_config200_response_data_instance = GetWebhookConfig200ResponseData.from_json(json)
# print the JSON string representation of the object
print(GetWebhookConfig200ResponseData.to_json())

# convert the object into a dict
get_webhook_config200_response_data_dict = get_webhook_config200_response_data_instance.to_dict()
# create an instance of GetWebhookConfig200ResponseData from a dict
get_webhook_config200_response_data_from_dict = GetWebhookConfig200ResponseData.from_dict(get_webhook_config200_response_data_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


