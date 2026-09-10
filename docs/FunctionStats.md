# FunctionStats


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**total_executions** | **int** |  | [optional] 
**successful_executions** | **int** |  | [optional] 
**failed_executions** | **int** |  | [optional] 
**avg_execution_time** | **float** |  | [optional] 
**last_execution** | **datetime** |  | [optional] 

## Example

```python
from mudbase.models.function_stats import FunctionStats

# TODO update the JSON string below
json = "{}"
# create an instance of FunctionStats from a JSON string
function_stats_instance = FunctionStats.from_json(json)
# print the JSON string representation of the object
print(FunctionStats.to_json())

# convert the object into a dict
function_stats_dict = function_stats_instance.to_dict()
# create an instance of FunctionStats from a dict
function_stats_from_dict = FunctionStats.from_dict(function_stats_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


