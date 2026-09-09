# EditMessageRequestE2ee

New opaque ciphertext (E2EE messages only)

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**version** | **int** |  | [optional] 
**scheme** | **str** |  | [optional] 
**ciphertext** | **str** |  | [optional] 
**nonce** | **str** |  | [optional] 
**ephemeral_public_key** | **str** |  | [optional] 
**sender_key_id** | **str** |  | [optional] 

## Example

```python
from mudbase.models.edit_message_request_e2ee import EditMessageRequestE2ee

# TODO update the JSON string below
json = "{}"
# create an instance of EditMessageRequestE2ee from a JSON string
edit_message_request_e2ee_instance = EditMessageRequestE2ee.from_json(json)
# print the JSON string representation of the object
print(EditMessageRequestE2ee.to_json())

# convert the object into a dict
edit_message_request_e2ee_dict = edit_message_request_e2ee_instance.to_dict()
# create an instance of EditMessageRequestE2ee from a dict
edit_message_request_e2ee_from_dict = EditMessageRequestE2ee.from_dict(edit_message_request_e2ee_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


