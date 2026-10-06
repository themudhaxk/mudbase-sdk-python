# TriggerFunctionWebhook200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**success** | **bool** |  | [optional] 
**triggered** | **int** | Number of functions triggered | [optional] 
**results** | **List[object]** |  | [optional] 

## Example

```python
from mudbase.models.trigger_function_webhook200_response import TriggerFunctionWebhook200Response

# TODO update the JSON string below
json = "{}"
# create an instance of TriggerFunctionWebhook200Response from a JSON string
trigger_function_webhook200_response_instance = TriggerFunctionWebhook200Response.from_json(json)
# print the JSON string representation of the object
print(TriggerFunctionWebhook200Response.to_json())

# convert the object into a dict
trigger_function_webhook200_response_dict = trigger_function_webhook200_response_instance.to_dict()
# create an instance of TriggerFunctionWebhook200Response from a dict
trigger_function_webhook200_response_from_dict = TriggerFunctionWebhook200Response.from_dict(trigger_function_webhook200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


