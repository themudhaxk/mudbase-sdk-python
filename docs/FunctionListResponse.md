# FunctionListResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**success** | **bool** |  | [optional] 
**data** | [**FunctionListResponseData**](FunctionListResponseData.md) |  | [optional] 

## Example

```python
from mudbase.models.function_list_response import FunctionListResponse

# TODO update the JSON string below
json = "{}"
# create an instance of FunctionListResponse from a JSON string
function_list_response_instance = FunctionListResponse.from_json(json)
# print the JSON string representation of the object
print(FunctionListResponse.to_json())

# convert the object into a dict
function_list_response_dict = function_list_response_instance.to_dict()
# create an instance of FunctionListResponse from a dict
function_list_response_from_dict = FunctionListResponse.from_dict(function_list_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


