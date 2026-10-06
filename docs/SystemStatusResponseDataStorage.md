# SystemStatusResponseDataStorage


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**used** | **int** |  | [optional] 
**available** | **int** |  | [optional] 
**percentage** | **float** |  | [optional] 

## Example

```python
from mudbase.models.system_status_response_data_storage import SystemStatusResponseDataStorage

# TODO update the JSON string below
json = "{}"
# create an instance of SystemStatusResponseDataStorage from a JSON string
system_status_response_data_storage_instance = SystemStatusResponseDataStorage.from_json(json)
# print the JSON string representation of the object
print(SystemStatusResponseDataStorage.to_json())

# convert the object into a dict
system_status_response_data_storage_dict = system_status_response_data_storage_instance.to_dict()
# create an instance of SystemStatusResponseDataStorage from a dict
system_status_response_data_storage_from_dict = SystemStatusResponseDataStorage.from_dict(system_status_response_data_storage_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


