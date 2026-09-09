# FunctionTrigger


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**type** | **str** | Trigger type | 
**event** | **str** | Event name (e.g. create, update, delete for document; uploaded, deleted for file) | [optional] 
**schedule** | **str** | For cron - minutely, hourly, daily, weekly, or custom cron expression | [optional] 
**path** | **str** | HTTP path for http triggers | [optional] 
**method** | **str** |  | [optional] 
**collection_id** | **str** | For document triggers - filter by collection | [optional] 
**bucket_id** | **str** | For file triggers - filter by bucket | [optional] 

## Example

```python
from mudbase.models.function_trigger import FunctionTrigger

# TODO update the JSON string below
json = "{}"
# create an instance of FunctionTrigger from a JSON string
function_trigger_instance = FunctionTrigger.from_json(json)
# print the JSON string representation of the object
print(FunctionTrigger.to_json())

# convert the object into a dict
function_trigger_dict = function_trigger_instance.to_dict()
# create an instance of FunctionTrigger from a dict
function_trigger_from_dict = FunctionTrigger.from_dict(function_trigger_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


