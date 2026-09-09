# MonitoringAnalyticsResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**period** | **str** |  | [optional] 
**granularity** | **str** |  | [optional] 
**days** | **int** | Present when rolling window used | [optional] 
**stats** | [**List[MonitoringAnalyticsResponseStatsInner]**](MonitoringAnalyticsResponseStatsInner.md) |  | [optional] 
**totals** | [**MonitoringAnalyticsResponseTotals**](MonitoringAnalyticsResponseTotals.md) |  | [optional] 

## Example

```python
from mudbase.models.monitoring_analytics_response import MonitoringAnalyticsResponse

# TODO update the JSON string below
json = "{}"
# create an instance of MonitoringAnalyticsResponse from a JSON string
monitoring_analytics_response_instance = MonitoringAnalyticsResponse.from_json(json)
# print the JSON string representation of the object
print(MonitoringAnalyticsResponse.to_json())

# convert the object into a dict
monitoring_analytics_response_dict = monitoring_analytics_response_instance.to_dict()
# create an instance of MonitoringAnalyticsResponse from a dict
monitoring_analytics_response_from_dict = MonitoringAnalyticsResponse.from_dict(monitoring_analytics_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


