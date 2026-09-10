# DeviceUnregisteredResponseData


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**removed** | **bool** | True if a matching token was removed; false if none was registered. | [optional] 

## Example

```python
from mudbase.models.device_unregistered_response_data import DeviceUnregisteredResponseData

# TODO update the JSON string below
json = "{}"
# create an instance of DeviceUnregisteredResponseData from a JSON string
device_unregistered_response_data_instance = DeviceUnregisteredResponseData.from_json(json)
# print the JSON string representation of the object
print(DeviceUnregisteredResponseData.to_json())

# convert the object into a dict
device_unregistered_response_data_dict = device_unregistered_response_data_instance.to_dict()
# create an instance of DeviceUnregisteredResponseData from a dict
device_unregistered_response_data_from_dict = DeviceUnregisteredResponseData.from_dict(device_unregistered_response_data_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


