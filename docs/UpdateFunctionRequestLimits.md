# UpdateFunctionRequestLimits


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**timeout** | **int** | Max execution time in ms (default 30000) | [optional] 
**max_payload_size** | **int** | Max payload size in bytes (default 1MB) | [optional] 
**max_executions_per_minute** | **int** |  | [optional] 
**max_executions_per_hour** | **int** |  | [optional] 

## Example

```python
from mudbase.models.update_function_request_limits import UpdateFunctionRequestLimits

# TODO update the JSON string below
json = "{}"
# create an instance of UpdateFunctionRequestLimits from a JSON string
update_function_request_limits_instance = UpdateFunctionRequestLimits.from_json(json)
# print the JSON string representation of the object
print(UpdateFunctionRequestLimits.to_json())

# convert the object into a dict
update_function_request_limits_dict = update_function_request_limits_instance.to_dict()
# create an instance of UpdateFunctionRequestLimits from a dict
update_function_request_limits_from_dict = UpdateFunctionRequestLimits.from_dict(update_function_request_limits_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


