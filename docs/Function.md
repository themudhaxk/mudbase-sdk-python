# Function


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** |  | [optional] 
**name** | **str** |  | [optional] 
**description** | **str** |  | [optional] 
**project_id** | **str** |  | [optional] 
**trigger** | [**FunctionTrigger**](FunctionTrigger.md) |  | [optional] 
**stats** | [**FunctionStats**](FunctionStats.md) |  | [optional] 
**is_active** | **bool** |  | [optional] 
**created_by** | **str** |  | [optional] 
**created_at** | **datetime** |  | [optional] 
**updated_at** | **datetime** |  | [optional] 

## Example

```python
from mudbase.models.function import Function

# TODO update the JSON string below
json = "{}"
# create an instance of Function from a JSON string
function_instance = Function.from_json(json)
# print the JSON string representation of the object
print(Function.to_json())

# convert the object into a dict
function_dict = function_instance.to_dict()
# create an instance of Function from a dict
function_from_dict = Function.from_dict(function_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


