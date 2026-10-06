# WebPushPublicKeyResponseData


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**enabled** | **bool** |  | [optional] 
**public_key** | **str** | The VAPID application-server public key, or null when native Web Push is not enabled.  | [optional] 

## Example

```python
from mudbase.models.web_push_public_key_response_data import WebPushPublicKeyResponseData

# TODO update the JSON string below
json = "{}"
# create an instance of WebPushPublicKeyResponseData from a JSON string
web_push_public_key_response_data_instance = WebPushPublicKeyResponseData.from_json(json)
# print the JSON string representation of the object
print(WebPushPublicKeyResponseData.to_json())

# convert the object into a dict
web_push_public_key_response_data_dict = web_push_public_key_response_data_instance.to_dict()
# create an instance of WebPushPublicKeyResponseData from a dict
web_push_public_key_response_data_from_dict = WebPushPublicKeyResponseData.from_dict(web_push_public_key_response_data_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


