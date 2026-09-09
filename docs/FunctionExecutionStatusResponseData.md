# FunctionExecutionStatusResponseData


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**execution_id** | **str** |  | [optional] 
**status** | **str** |  | [optional] 
**duration_ms** | **int** | Duration in milliseconds (null until completed) | [optional] 
**result** | **object** |  | [optional] 
**error** | **str** |  | [optional] 
**error_class** | **str** |  | [optional] 
**logs** | [**FunctionExecutionStatusResponseDataLogs**](FunctionExecutionStatusResponseDataLogs.md) |  | [optional] 
**machine** | **object** |  | [optional] 
**created_at** | **datetime** |  | [optional] 
**started_at** | **datetime** |  | [optional] 
**completed_at** | **datetime** |  | [optional] 

## Example

```python
from mudbase.models.function_execution_status_response_data import FunctionExecutionStatusResponseData

# TODO update the JSON string below
json = "{}"
# create an instance of FunctionExecutionStatusResponseData from a JSON string
function_execution_status_response_data_instance = FunctionExecutionStatusResponseData.from_json(json)
# print the JSON string representation of the object
print(FunctionExecutionStatusResponseData.to_json())

# convert the object into a dict
function_execution_status_response_data_dict = function_execution_status_response_data_instance.to_dict()
# create an instance of FunctionExecutionStatusResponseData from a dict
function_execution_status_response_data_from_dict = FunctionExecutionStatusResponseData.from_dict(function_execution_status_response_data_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


