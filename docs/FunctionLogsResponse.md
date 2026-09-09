# FunctionLogsResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**success** | **bool** |  | [optional] 
**data** | [**FunctionLogsResponseData**](FunctionLogsResponseData.md) |  | [optional] 

## Example

```python
from mudbase.models.function_logs_response import FunctionLogsResponse

# TODO update the JSON string below
json = "{}"
# create an instance of FunctionLogsResponse from a JSON string
function_logs_response_instance = FunctionLogsResponse.from_json(json)
# print the JSON string representation of the object
print(FunctionLogsResponse.to_json())

# convert the object into a dict
function_logs_response_dict = function_logs_response_instance.to_dict()
# create an instance of FunctionLogsResponse from a dict
function_logs_response_from_dict = FunctionLogsResponse.from_dict(function_logs_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


