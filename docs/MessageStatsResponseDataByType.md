# MessageStatsResponseDataByType


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**push** | **int** |  | [optional] 
**email** | **int** |  | [optional] 
**sms** | **int** |  | [optional] 

## Example

```python
from mudbase.models.message_stats_response_data_by_type import MessageStatsResponseDataByType

# TODO update the JSON string below
json = "{}"
# create an instance of MessageStatsResponseDataByType from a JSON string
message_stats_response_data_by_type_instance = MessageStatsResponseDataByType.from_json(json)
# print the JSON string representation of the object
print(MessageStatsResponseDataByType.to_json())

# convert the object into a dict
message_stats_response_data_by_type_dict = message_stats_response_data_by_type_instance.to_dict()
# create an instance of MessageStatsResponseDataByType from a dict
message_stats_response_data_by_type_from_dict = MessageStatsResponseDataByType.from_dict(message_stats_response_data_by_type_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


