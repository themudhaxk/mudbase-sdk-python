# DeviceUnregisteredResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**success** | **bool** |  | [optional] 
**data** | [**DeviceUnregisteredResponseData**](DeviceUnregisteredResponseData.md) |  | [optional] 

## Example

```python
from mudbase.models.device_unregistered_response import DeviceUnregisteredResponse

# TODO update the JSON string below
json = "{}"
# create an instance of DeviceUnregisteredResponse from a JSON string
device_unregistered_response_instance = DeviceUnregisteredResponse.from_json(json)
# print the JSON string representation of the object
print(DeviceUnregisteredResponse.to_json())

# convert the object into a dict
device_unregistered_response_dict = device_unregistered_response_instance.to_dict()
# create an instance of DeviceUnregisteredResponse from a dict
device_unregistered_response_from_dict = DeviceUnregisteredResponse.from_dict(device_unregistered_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


