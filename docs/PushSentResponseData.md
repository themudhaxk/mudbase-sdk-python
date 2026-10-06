# PushSentResponseData


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**success** | **bool** | True when at least one recipient across any channel was delivered to. | [optional] 
**message_id** | **str** |  | [optional] 
**success_count** | **int** |  | [optional] 
**failure_count** | **int** |  | [optional] 
**channels** | [**PushSentResponseDataChannels**](PushSentResponseDataChannels.md) |  | [optional] 
**rejected_tokens** | **List[str]** | Device tokens that were passed but are not registered to the project, and so were dropped. Omitted when empty.  | [optional] 

## Example

```python
from mudbase.models.push_sent_response_data import PushSentResponseData

# TODO update the JSON string below
json = "{}"
# create an instance of PushSentResponseData from a JSON string
push_sent_response_data_instance = PushSentResponseData.from_json(json)
# print the JSON string representation of the object
print(PushSentResponseData.to_json())

# convert the object into a dict
push_sent_response_data_dict = push_sent_response_data_instance.to_dict()
# create an instance of PushSentResponseData from a dict
push_sent_response_data_from_dict = PushSentResponseData.from_dict(push_sent_response_data_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


