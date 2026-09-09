# FunctionLogsResponseData


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**executions** | [**List[FunctionExecution]**](FunctionExecution.md) |  | [optional] 
**stats** | [**FunctionStats**](FunctionStats.md) |  | [optional] 

## Example

```python
from mudbase.models.function_logs_response_data import FunctionLogsResponseData

# TODO update the JSON string below
json = "{}"
# create an instance of FunctionLogsResponseData from a JSON string
function_logs_response_data_instance = FunctionLogsResponseData.from_json(json)
# print the JSON string representation of the object
print(FunctionLogsResponseData.to_json())

# convert the object into a dict
function_logs_response_data_dict = function_logs_response_data_instance.to_dict()
# create an instance of FunctionLogsResponseData from a dict
function_logs_response_data_from_dict = FunctionLogsResponseData.from_dict(function_logs_response_data_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


