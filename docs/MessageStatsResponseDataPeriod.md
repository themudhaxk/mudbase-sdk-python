# MessageStatsResponseDataPeriod


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**start_date** | **datetime** |  | [optional] 
**end_date** | **datetime** |  | [optional] 

## Example

```python
from mudbase.models.message_stats_response_data_period import MessageStatsResponseDataPeriod

# TODO update the JSON string below
json = "{}"
# create an instance of MessageStatsResponseDataPeriod from a JSON string
message_stats_response_data_period_instance = MessageStatsResponseDataPeriod.from_json(json)
# print the JSON string representation of the object
print(MessageStatsResponseDataPeriod.to_json())

# convert the object into a dict
message_stats_response_data_period_dict = message_stats_response_data_period_instance.to_dict()
# create an instance of MessageStatsResponseDataPeriod from a dict
message_stats_response_data_period_from_dict = MessageStatsResponseDataPeriod.from_dict(message_stats_response_data_period_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


