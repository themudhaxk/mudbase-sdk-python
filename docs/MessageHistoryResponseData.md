# MessageHistoryResponseData


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**messages** | [**List[Message]**](Message.md) |  | [optional] 
**pagination** | [**Pagination**](Pagination.md) |  | [optional] 

## Example

```python
from mudbase.models.message_history_response_data import MessageHistoryResponseData

# TODO update the JSON string below
json = "{}"
# create an instance of MessageHistoryResponseData from a JSON string
message_history_response_data_instance = MessageHistoryResponseData.from_json(json)
# print the JSON string representation of the object
print(MessageHistoryResponseData.to_json())

# convert the object into a dict
message_history_response_data_dict = message_history_response_data_instance.to_dict()
# create an instance of MessageHistoryResponseData from a dict
message_history_response_data_from_dict = MessageHistoryResponseData.from_dict(message_history_response_data_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


