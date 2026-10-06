# SystemStatusResponseDataMemory


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**used** | **int** |  | [optional] 
**total** | **int** |  | [optional] 
**percentage** | **float** |  | [optional] 

## Example

```python
from mudbase.models.system_status_response_data_memory import SystemStatusResponseDataMemory

# TODO update the JSON string below
json = "{}"
# create an instance of SystemStatusResponseDataMemory from a JSON string
system_status_response_data_memory_instance = SystemStatusResponseDataMemory.from_json(json)
# print the JSON string representation of the object
print(SystemStatusResponseDataMemory.to_json())

# convert the object into a dict
system_status_response_data_memory_dict = system_status_response_data_memory_instance.to_dict()
# create an instance of SystemStatusResponseDataMemory from a dict
system_status_response_data_memory_from_dict = SystemStatusResponseDataMemory.from_dict(system_status_response_data_memory_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


