# MessageSentResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**success** | **bool** |  | [optional] 
**data** | [**MessageSentResponseData**](MessageSentResponseData.md) |  | [optional] 

## Example

```python
from mudbase.models.message_sent_response import MessageSentResponse

# TODO update the JSON string below
json = "{}"
# create an instance of MessageSentResponse from a JSON string
message_sent_response_instance = MessageSentResponse.from_json(json)
# print the JSON string representation of the object
print(MessageSentResponse.to_json())

# convert the object into a dict
message_sent_response_dict = message_sent_response_instance.to_dict()
# create an instance of MessageSentResponse from a dict
message_sent_response_from_dict = MessageSentResponse.from_dict(message_sent_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


