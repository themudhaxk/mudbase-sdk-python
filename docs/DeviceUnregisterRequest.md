# DeviceUnregisterRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**token** | **str** | The device push token to remove from the project. | 

## Example

```python
from mudbase.models.device_unregister_request import DeviceUnregisterRequest

# TODO update the JSON string below
json = "{}"
# create an instance of DeviceUnregisterRequest from a JSON string
device_unregister_request_instance = DeviceUnregisterRequest.from_json(json)
# print the JSON string representation of the object
print(DeviceUnregisterRequest.to_json())

# convert the object into a dict
device_unregister_request_dict = device_unregister_request_instance.to_dict()
# create an instance of DeviceUnregisterRequest from a dict
device_unregister_request_from_dict = DeviceUnregisterRequest.from_dict(device_unregister_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


