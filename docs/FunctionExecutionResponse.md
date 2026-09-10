# FunctionExecutionResponse

Response from Execute function / Simulate trigger. Both endpoints are async (202) and only hand back an executionId — see FunctionExecutionStatusResponse for the real outcome. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**success** | **bool** |  | [optional] 
**data** | [**FunctionExecutionResponseData**](FunctionExecutionResponseData.md) |  | [optional] 

## Example

```python
from mudbase.models.function_execution_response import FunctionExecutionResponse

# TODO update the JSON string below
json = "{}"
# create an instance of FunctionExecutionResponse from a JSON string
function_execution_response_instance = FunctionExecutionResponse.from_json(json)
# print the JSON string representation of the object
print(FunctionExecutionResponse.to_json())

# convert the object into a dict
function_execution_response_dict = function_execution_response_instance.to_dict()
# create an instance of FunctionExecutionResponse from a dict
function_execution_response_from_dict = FunctionExecutionResponse.from_dict(function_execution_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


