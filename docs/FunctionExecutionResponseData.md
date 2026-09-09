# FunctionExecutionResponseData


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**execution_id** | **str** |  | [optional] 
**status** | **str** |  | [optional] 

## Example

```python
from mudbase.models.function_execution_response_data import FunctionExecutionResponseData

# TODO update the JSON string below
json = "{}"
# create an instance of FunctionExecutionResponseData from a JSON string
function_execution_response_data_instance = FunctionExecutionResponseData.from_json(json)
# print the JSON string representation of the object
print(FunctionExecutionResponseData.to_json())

# convert the object into a dict
function_execution_response_data_dict = function_execution_response_data_instance.to_dict()
# create an instance of FunctionExecutionResponseData from a dict
function_execution_response_data_from_dict = FunctionExecutionResponseData.from_dict(function_execution_response_data_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


