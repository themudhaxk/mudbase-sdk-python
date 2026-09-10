# WebPushPublicKeyResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**success** | **bool** |  | [optional] 
**data** | [**WebPushPublicKeyResponseData**](WebPushPublicKeyResponseData.md) |  | [optional] 

## Example

```python
from mudbase.models.web_push_public_key_response import WebPushPublicKeyResponse

# TODO update the JSON string below
json = "{}"
# create an instance of WebPushPublicKeyResponse from a JSON string
web_push_public_key_response_instance = WebPushPublicKeyResponse.from_json(json)
# print the JSON string representation of the object
print(WebPushPublicKeyResponse.to_json())

# convert the object into a dict
web_push_public_key_response_dict = web_push_public_key_response_instance.to_dict()
# create an instance of WebPushPublicKeyResponse from a dict
web_push_public_key_response_from_dict = WebPushPublicKeyResponse.from_dict(web_push_public_key_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


