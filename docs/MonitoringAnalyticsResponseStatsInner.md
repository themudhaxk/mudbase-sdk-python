# MonitoringAnalyticsResponseStatsInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**var_date** | **str** |  | [optional] 
**api_calls** | **int** |  | [optional] 
**db_reads** | **int** |  | [optional] 
**db_writes** | **int** |  | [optional] 
**storage** | **int** |  | [optional] 
**bandwidth** | **int** |  | [optional] 

## Example

```python
from mudbase.models.monitoring_analytics_response_stats_inner import MonitoringAnalyticsResponseStatsInner

# TODO update the JSON string below
json = "{}"
# create an instance of MonitoringAnalyticsResponseStatsInner from a JSON string
monitoring_analytics_response_stats_inner_instance = MonitoringAnalyticsResponseStatsInner.from_json(json)
# print the JSON string representation of the object
print(MonitoringAnalyticsResponseStatsInner.to_json())

# convert the object into a dict
monitoring_analytics_response_stats_inner_dict = monitoring_analytics_response_stats_inner_instance.to_dict()
# create an instance of MonitoringAnalyticsResponseStatsInner from a dict
monitoring_analytics_response_stats_inner_from_dict = MonitoringAnalyticsResponseStatsInner.from_dict(monitoring_analytics_response_stats_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


