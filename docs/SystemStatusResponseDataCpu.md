# SystemStatusResponseDataCpu


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**usage** | **float** |  | [optional] 
**cores** | **int** |  | [optional] 

## Example

```python
from mudbase.models.system_status_response_data_cpu import SystemStatusResponseDataCpu

# TODO update the JSON string below
json = "{}"
# create an instance of SystemStatusResponseDataCpu from a JSON string
system_status_response_data_cpu_instance = SystemStatusResponseDataCpu.from_json(json)
# print the JSON string representation of the object
print(SystemStatusResponseDataCpu.to_json())

# convert the object into a dict
system_status_response_data_cpu_dict = system_status_response_data_cpu_instance.to_dict()
# create an instance of SystemStatusResponseDataCpu from a dict
system_status_response_data_cpu_from_dict = SystemStatusResponseDataCpu.from_dict(system_status_response_data_cpu_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


