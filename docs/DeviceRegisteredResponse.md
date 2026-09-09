# DeviceRegisteredResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**success** | **bool** |  | [optional] 
**data** | [**DeviceRegisteredResponseData**](DeviceRegisteredResponseData.md) |  | [optional] 

## Example

```python
from mudbase.models.device_registered_response import DeviceRegisteredResponse

# TODO update the JSON string below
json = "{}"
# create an instance of DeviceRegisteredResponse from a JSON string
device_registered_response_instance = DeviceRegisteredResponse.from_json(json)
# print the JSON string representation of the object
print(DeviceRegisteredResponse.to_json())

# convert the object into a dict
device_registered_response_dict = device_registered_response_instance.to_dict()
# create an instance of DeviceRegisteredResponse from a dict
device_registered_response_from_dict = DeviceRegisteredResponse.from_dict(device_registered_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


