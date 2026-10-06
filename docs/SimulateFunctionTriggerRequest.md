# SimulateFunctionTriggerRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**trigger** | **object** | Simulated trigger (type, event) | [optional] 
**event_context** | **object** | Simulated event context (document, file, webhook, message) | [optional] 
**payload** | **object** | Additional payload | [optional] 

## Example

```python
from mudbase.models.simulate_function_trigger_request import SimulateFunctionTriggerRequest

# TODO update the JSON string below
json = "{}"
# create an instance of SimulateFunctionTriggerRequest from a JSON string
simulate_function_trigger_request_instance = SimulateFunctionTriggerRequest.from_json(json)
# print the JSON string representation of the object
print(SimulateFunctionTriggerRequest.to_json())

# convert the object into a dict
simulate_function_trigger_request_dict = simulate_function_trigger_request_instance.to_dict()
# create an instance of SimulateFunctionTriggerRequest from a dict
simulate_function_trigger_request_from_dict = SimulateFunctionTriggerRequest.from_dict(simulate_function_trigger_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


