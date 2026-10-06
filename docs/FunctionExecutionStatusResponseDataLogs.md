# FunctionExecutionStatusResponseDataLogs


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**stdout** | **str** |  | [optional] 
**stderr** | **str** |  | [optional] 
**truncated** | **bool** |  | [optional] 
**bytes** | **int** |  | [optional] 

## Example

```python
from mudbase.models.function_execution_status_response_data_logs import FunctionExecutionStatusResponseDataLogs

# TODO update the JSON string below
json = "{}"
# create an instance of FunctionExecutionStatusResponseDataLogs from a JSON string
function_execution_status_response_data_logs_instance = FunctionExecutionStatusResponseDataLogs.from_json(json)
# print the JSON string representation of the object
print(FunctionExecutionStatusResponseDataLogs.to_json())

# convert the object into a dict
function_execution_status_response_data_logs_dict = function_execution_status_response_data_logs_instance.to_dict()
# create an instance of FunctionExecutionStatusResponseDataLogs from a dict
function_execution_status_response_data_logs_from_dict = FunctionExecutionStatusResponseDataLogs.from_dict(function_execution_status_response_data_logs_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


