# FunctionExecutionStatusResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**success** | **bool** |  | [optional] 
**data** | [**FunctionExecutionStatusResponseData**](FunctionExecutionStatusResponseData.md) |  | [optional] 

## Example

```python
from mudbase.models.function_execution_status_response import FunctionExecutionStatusResponse

# TODO update the JSON string below
json = "{}"
# create an instance of FunctionExecutionStatusResponse from a JSON string
function_execution_status_response_instance = FunctionExecutionStatusResponse.from_json(json)
# print the JSON string representation of the object
print(FunctionExecutionStatusResponse.to_json())

# convert the object into a dict
function_execution_status_response_dict = function_execution_status_response_instance.to_dict()
# create an instance of FunctionExecutionStatusResponse from a dict
function_execution_status_response_from_dict = FunctionExecutionStatusResponse.from_dict(function_execution_status_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


