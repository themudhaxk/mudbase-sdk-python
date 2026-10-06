# SendMessageRequestE2ee

Opaque end-to-end encrypted payload (base64 ciphertext). Server cannot decrypt. Only for type=text.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**version** | **int** |  | [optional] [default to 1]
**scheme** | **str** |  | [optional] 
**ciphertext** | **str** | Base64-encoded ciphertext | [optional] 
**nonce** | **str** |  | [optional] 
**ephemeral_public_key** | **str** |  | [optional] 
**sender_key_id** | **str** |  | [optional] 

## Example

```python
from mudbase.models.send_message_request_e2ee import SendMessageRequestE2ee

# TODO update the JSON string below
json = "{}"
# create an instance of SendMessageRequestE2ee from a JSON string
send_message_request_e2ee_instance = SendMessageRequestE2ee.from_json(json)
# print the JSON string representation of the object
print(SendMessageRequestE2ee.to_json())

# convert the object into a dict
send_message_request_e2ee_dict = send_message_request_e2ee_instance.to_dict()
# create an instance of SendMessageRequestE2ee from a dict
send_message_request_e2ee_from_dict = SendMessageRequestE2ee.from_dict(send_message_request_e2ee_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


