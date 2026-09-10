# SystemStatusResponseData


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**uptime** | **int** |  | [optional] 
**memory** | [**SystemStatusResponseDataMemory**](SystemStatusResponseDataMemory.md) |  | [optional] 
**cpu** | [**SystemStatusResponseDataCpu**](SystemStatusResponseDataCpu.md) |  | [optional] 
**requests** | [**SystemStatusResponseDataRequests**](SystemStatusResponseDataRequests.md) |  | [optional] 
**database** | [**SystemStatusResponseDataDatabase**](SystemStatusResponseDataDatabase.md) |  | [optional] 
**storage** | [**SystemStatusResponseDataStorage**](SystemStatusResponseDataStorage.md) |  | [optional] 

## Example

```python
from mudbase.models.system_status_response_data import SystemStatusResponseData

# TODO update the JSON string below
json = "{}"
# create an instance of SystemStatusResponseData from a JSON string
system_status_response_data_instance = SystemStatusResponseData.from_json(json)
# print the JSON string representation of the object
print(SystemStatusResponseData.to_json())

# convert the object into a dict
system_status_response_data_dict = system_status_response_data_instance.to_dict()
# create an instance of SystemStatusResponseData from a dict
system_status_response_data_from_dict = SystemStatusResponseData.from_dict(system_status_response_data_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


