# DeviceToken


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**token** | **str** |  | [optional] 
**platform** | **str** |  | [optional] 
**last_seen_at** | **datetime** |  | [optional] 
**created_at** | **datetime** |  | [optional] 

## Example

```python
from mudbase.models.device_token import DeviceToken

# TODO update the JSON string below
json = "{}"
# create an instance of DeviceToken from a JSON string
device_token_instance = DeviceToken.from_json(json)
# print the JSON string representation of the object
print(DeviceToken.to_json())

# convert the object into a dict
device_token_dict = device_token_instance.to_dict()
# create an instance of DeviceToken from a dict
device_token_from_dict = DeviceToken.from_dict(device_token_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


