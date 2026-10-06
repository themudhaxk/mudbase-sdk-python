# SystemStatusResponseDataDatabase


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**connections** | **int** |  | [optional] 
**max_connections** | **int** |  | [optional] 
**response_time** | **int** |  | [optional] 

## Example

```python
from mudbase.models.system_status_response_data_database import SystemStatusResponseDataDatabase

# TODO update the JSON string below
json = "{}"
# create an instance of SystemStatusResponseDataDatabase from a JSON string
system_status_response_data_database_instance = SystemStatusResponseDataDatabase.from_json(json)
# print the JSON string representation of the object
print(SystemStatusResponseDataDatabase.to_json())

# convert the object into a dict
system_status_response_data_database_dict = system_status_response_data_database_instance.to_dict()
# create an instance of SystemStatusResponseDataDatabase from a dict
system_status_response_data_database_from_dict = SystemStatusResponseDataDatabase.from_dict(system_status_response_data_database_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


