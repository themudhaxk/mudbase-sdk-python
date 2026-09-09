# FunctionExecution


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** |  | [optional] 
**executed_at** | **datetime** |  | [optional] 
**execution_time** | **int** |  | [optional] 
**success** | **bool** |  | [optional] 
**payload** | **object** |  | [optional] 
**result** | **object** |  | [optional] 
**error** | **str** |  | [optional] 
**trigger_type** | **str** |  | [optional] 
**trigger_event** | **str** |  | [optional] 
**invoked_by** | **str** |  | [optional] 
**retry_count** | **int** |  | [optional] 

## Example

```python
from mudbase.models.function_execution import FunctionExecution

# TODO update the JSON string below
json = "{}"
# create an instance of FunctionExecution from a JSON string
function_execution_instance = FunctionExecution.from_json(json)
# print the JSON string representation of the object
print(FunctionExecution.to_json())

# convert the object into a dict
function_execution_dict = function_execution_instance.to_dict()
# create an instance of FunctionExecution from a dict
function_execution_from_dict = FunctionExecution.from_dict(function_execution_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


