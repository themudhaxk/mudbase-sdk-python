# GetWebhookConfig200ResponseDataTransformationsInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**type** | **str** |  | [optional] 
**config** | **object** | Transformation-specific configuration (shape depends on &#x60;type&#x60;) | [optional] 

## Example

```python
from mudbase.models.get_webhook_config200_response_data_transformations_inner import GetWebhookConfig200ResponseDataTransformationsInner

# TODO update the JSON string below
json = "{}"
# create an instance of GetWebhookConfig200ResponseDataTransformationsInner from a JSON string
get_webhook_config200_response_data_transformations_inner_instance = GetWebhookConfig200ResponseDataTransformationsInner.from_json(json)
# print the JSON string representation of the object
print(GetWebhookConfig200ResponseDataTransformationsInner.to_json())

# convert the object into a dict
get_webhook_config200_response_data_transformations_inner_dict = get_webhook_config200_response_data_transformations_inner_instance.to_dict()
# create an instance of GetWebhookConfig200ResponseDataTransformationsInner from a dict
get_webhook_config200_response_data_transformations_inner_from_dict = GetWebhookConfig200ResponseDataTransformationsInner.from_dict(get_webhook_config200_response_data_transformations_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


