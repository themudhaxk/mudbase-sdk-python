# TriggerFunctionWebhook400Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**success** | **bool** |  | [optional] 
**error** | **str** |  | [optional] 

## Example

```python
from mudbase.models.trigger_function_webhook400_response import TriggerFunctionWebhook400Response

# TODO update the JSON string below
json = "{}"
# create an instance of TriggerFunctionWebhook400Response from a JSON string
trigger_function_webhook400_response_instance = TriggerFunctionWebhook400Response.from_json(json)
# print the JSON string representation of the object
print(TriggerFunctionWebhook400Response.to_json())

# convert the object into a dict
trigger_function_webhook400_response_dict = trigger_function_webhook400_response_instance.to_dict()
# create an instance of TriggerFunctionWebhook400Response from a dict
trigger_function_webhook400_response_from_dict = TriggerFunctionWebhook400Response.from_dict(trigger_function_webhook400_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


