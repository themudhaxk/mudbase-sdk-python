# SystemStatusResponseDataRequests


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**total** | **int** |  | [optional] 
**successful** | **int** |  | [optional] 
**errors** | **int** |  | [optional] 
**error_rate** | **float** |  | [optional] 

## Example

```python
from mudbase.models.system_status_response_data_requests import SystemStatusResponseDataRequests

# TODO update the JSON string below
json = "{}"
# create an instance of SystemStatusResponseDataRequests from a JSON string
system_status_response_data_requests_instance = SystemStatusResponseDataRequests.from_json(json)
# print the JSON string representation of the object
print(SystemStatusResponseDataRequests.to_json())

# convert the object into a dict
system_status_response_data_requests_dict = system_status_response_data_requests_instance.to_dict()
# create an instance of SystemStatusResponseDataRequests from a dict
system_status_response_data_requests_from_dict = SystemStatusResponseDataRequests.from_dict(system_status_response_data_requests_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


