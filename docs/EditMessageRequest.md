# EditMessageRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**content** | **str** | New plaintext (non-E2EE messages only) | [optional] 
**e2ee** | [**EditMessageRequestE2ee**](EditMessageRequestE2ee.md) |  | [optional] 

## Example

```python
from mudbase.models.edit_message_request import EditMessageRequest

# TODO update the JSON string below
json = "{}"
# create an instance of EditMessageRequest from a JSON string
edit_message_request_instance = EditMessageRequest.from_json(json)
# print the JSON string representation of the object
print(EditMessageRequest.to_json())

# convert the object into a dict
edit_message_request_dict = edit_message_request_instance.to_dict()
# create an instance of EditMessageRequest from a dict
edit_message_request_from_dict = EditMessageRequest.from_dict(edit_message_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


