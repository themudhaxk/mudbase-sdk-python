# MessageHistoryResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**success** | **bool** |  | [optional] 
**data** | [**MessageHistoryResponseData**](MessageHistoryResponseData.md) |  | [optional] 

## Example

```python
from mudbase.models.message_history_response import MessageHistoryResponse

# TODO update the JSON string below
json = "{}"
# create an instance of MessageHistoryResponse from a JSON string
message_history_response_instance = MessageHistoryResponse.from_json(json)
# print the JSON string representation of the object
print(MessageHistoryResponse.to_json())

# convert the object into a dict
message_history_response_dict = message_history_response_instance.to_dict()
# create an instance of MessageHistoryResponse from a dict
message_history_response_from_dict = MessageHistoryResponse.from_dict(message_history_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


