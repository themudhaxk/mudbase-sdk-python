# MessageStatsResponseData


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**total_messages** | **int** |  | [optional] 
**by_type** | [**MessageStatsResponseDataByType**](MessageStatsResponseDataByType.md) |  | [optional] 
**by_status** | [**MessageStatsResponseDataByStatus**](MessageStatsResponseDataByStatus.md) |  | [optional] 
**success_rate** | **float** |  | [optional] 
**period** | [**MessageStatsResponseDataPeriod**](MessageStatsResponseDataPeriod.md) |  | [optional] 

## Example

```python
from mudbase.models.message_stats_response_data import MessageStatsResponseData

# TODO update the JSON string below
json = "{}"
# create an instance of MessageStatsResponseData from a JSON string
message_stats_response_data_instance = MessageStatsResponseData.from_json(json)
# print the JSON string representation of the object
print(MessageStatsResponseData.to_json())

# convert the object into a dict
message_stats_response_data_dict = message_stats_response_data_instance.to_dict()
# create an instance of MessageStatsResponseData from a dict
message_stats_response_data_from_dict = MessageStatsResponseData.from_dict(message_stats_response_data_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


