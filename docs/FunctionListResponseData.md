# FunctionListResponseData


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**functions** | [**List[Function]**](Function.md) |  | [optional] 
**pagination** | [**Pagination**](Pagination.md) |  | [optional] 

## Example

```python
from mudbase.models.function_list_response_data import FunctionListResponseData

# TODO update the JSON string below
json = "{}"
# create an instance of FunctionListResponseData from a JSON string
function_list_response_data_instance = FunctionListResponseData.from_json(json)
# print the JSON string representation of the object
print(FunctionListResponseData.to_json())

# convert the object into a dict
function_list_response_data_dict = function_list_response_data_instance.to_dict()
# create an instance of FunctionListResponseData from a dict
function_list_response_data_from_dict = FunctionListResponseData.from_dict(function_list_response_data_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


