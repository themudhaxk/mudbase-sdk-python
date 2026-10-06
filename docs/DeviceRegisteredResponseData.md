# DeviceRegisteredResponseData


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**token** | **str** |  | [optional] 
**platform** | **str** |  | [optional] 
**last_seen_at** | **datetime** |  | [optional] 

## Example

```python
from mudbase.models.device_registered_response_data import DeviceRegisteredResponseData

# TODO update the JSON string below
json = "{}"
# create an instance of DeviceRegisteredResponseData from a JSON string
device_registered_response_data_instance = DeviceRegisteredResponseData.from_json(json)
# print the JSON string representation of the object
print(DeviceRegisteredResponseData.to_json())

# convert the object into a dict
device_registered_response_data_dict = device_registered_response_data_instance.to_dict()
# create an instance of DeviceRegisteredResponseData from a dict
device_registered_response_data_from_dict = DeviceRegisteredResponseData.from_dict(device_registered_response_data_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


