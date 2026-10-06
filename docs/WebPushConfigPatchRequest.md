# WebPushConfigPatchRequest

All fields optional. `enabled` toggles native Web Push (and provisions a keypair on first enable); `rotateKeys` regenerates the keypair (invalidating existing subscriptions); `subject` sets the RFC 8292 contact URI. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**enabled** | **bool** |  | [optional] 
**rotate_keys** | **bool** |  | [optional] 
**subject** | **str** | A &#x60;mailto:&#x60; address or an &#x60;https&#x60; URL. | [optional] 

## Example

```python
from mudbase.models.web_push_config_patch_request import WebPushConfigPatchRequest

# TODO update the JSON string below
json = "{}"
# create an instance of WebPushConfigPatchRequest from a JSON string
web_push_config_patch_request_instance = WebPushConfigPatchRequest.from_json(json)
# print the JSON string representation of the object
print(WebPushConfigPatchRequest.to_json())

# convert the object into a dict
web_push_config_patch_request_dict = web_push_config_patch_request_instance.to_dict()
# create an instance of WebPushConfigPatchRequest from a dict
web_push_config_patch_request_from_dict = WebPushConfigPatchRequest.from_dict(web_push_config_patch_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


