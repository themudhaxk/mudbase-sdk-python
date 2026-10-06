# PutChatE2eeKeyRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**identity_public_key** | **str** | Base64-encoded public key (algorithm defined by client; opaque to server) | 
**key_version** | **int** | Optional; defaults to incrementing stored version | [optional] 

## Example

```python
from mudbase.models.put_chat_e2ee_key_request import PutChatE2eeKeyRequest

# TODO update the JSON string below
json = "{}"
# create an instance of PutChatE2eeKeyRequest from a JSON string
put_chat_e2ee_key_request_instance = PutChatE2eeKeyRequest.from_json(json)
# print the JSON string representation of the object
print(PutChatE2eeKeyRequest.to_json())

# convert the object into a dict
put_chat_e2ee_key_request_dict = put_chat_e2ee_key_request_instance.to_dict()
# create an instance of PutChatE2eeKeyRequest from a dict
put_chat_e2ee_key_request_from_dict = PutChatE2eeKeyRequest.from_dict(put_chat_e2ee_key_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


