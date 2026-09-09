# MessageSentResponseData


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** |  | [optional] 
**type** | **str** |  | [optional] 
**status** | **str** |  | [optional] 
**recipients** | **int** |  | [optional] 
**success_count** | **int** |  | [optional] 
**failure_count** | **int** |  | [optional] 
**message_id** | **str** |  | [optional] 
**sent_at** | **datetime** |  | [optional] 

## Example

```python
from mudbase.models.message_sent_response_data import MessageSentResponseData

# TODO update the JSON string below
json = "{}"
# create an instance of MessageSentResponseData from a JSON string
message_sent_response_data_instance = MessageSentResponseData.from_json(json)
# print the JSON string representation of the object
print(MessageSentResponseData.to_json())

# convert the object into a dict
message_sent_response_data_dict = message_sent_response_data_instance.to_dict()
# create an instance of MessageSentResponseData from a dict
message_sent_response_data_from_dict = MessageSentResponseData.from_dict(message_sent_response_data_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


