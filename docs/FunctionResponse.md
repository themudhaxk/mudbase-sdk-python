# FunctionResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**success** | **bool** |  | [optional] 
**data** | [**Function**](Function.md) |  | [optional] 

## Example

```python
from mudbase.models.function_response import FunctionResponse

# TODO update the JSON string below
json = "{}"
# create an instance of FunctionResponse from a JSON string
function_response_instance = FunctionResponse.from_json(json)
# print the JSON string representation of the object
print(FunctionResponse.to_json())

# convert the object into a dict
function_response_dict = function_response_instance.to_dict()
# create an instance of FunctionResponse from a dict
function_response_from_dict = FunctionResponse.from_dict(function_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


