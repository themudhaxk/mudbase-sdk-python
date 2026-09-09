# MessageStatsResponseDataByStatus


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**sent** | **int** |  | [optional] 
**failed** | **int** |  | [optional] 
**pending** | **int** |  | [optional] 

## Example

```python
from mudbase.models.message_stats_response_data_by_status import MessageStatsResponseDataByStatus

# TODO update the JSON string below
json = "{}"
# create an instance of MessageStatsResponseDataByStatus from a JSON string
message_stats_response_data_by_status_instance = MessageStatsResponseDataByStatus.from_json(json)
# print the JSON string representation of the object
print(MessageStatsResponseDataByStatus.to_json())

# convert the object into a dict
message_stats_response_data_by_status_dict = message_stats_response_data_by_status_instance.to_dict()
# create an instance of MessageStatsResponseDataByStatus from a dict
message_stats_response_data_by_status_from_dict = MessageStatsResponseDataByStatus.from_dict(message_stats_response_data_by_status_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


