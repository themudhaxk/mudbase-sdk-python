# GetWebhookConfig404Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**success** | **bool** |  | [optional] 
**error** | **str** |  | [optional] 

## Example

```python
from mudbase.models.get_webhook_config404_response import GetWebhookConfig404Response

# TODO update the JSON string below
json = "{}"
# create an instance of GetWebhookConfig404Response from a JSON string
get_webhook_config404_response_instance = GetWebhookConfig404Response.from_json(json)
# print the JSON string representation of the object
print(GetWebhookConfig404Response.to_json())

# convert the object into a dict
get_webhook_config404_response_dict = get_webhook_config404_response_instance.to_dict()
# create an instance of GetWebhookConfig404Response from a dict
get_webhook_config404_response_from_dict = GetWebhookConfig404Response.from_dict(get_webhook_config404_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


