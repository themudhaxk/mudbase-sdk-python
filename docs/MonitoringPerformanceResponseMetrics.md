# MonitoringPerformanceResponseMetrics


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**total_requests** | **int** |  | [optional] 
**avg_response_time** | **float** |  | [optional] 
**min_response_time** | **float** |  | [optional] 
**max_response_time** | **float** |  | [optional] 
**error_count** | **int** |  | [optional] 
**success_count** | **int** |  | [optional] 
**success_rate** | **float** |  | [optional] 
**error_rate** | **float** |  | [optional] 
**latency_source** | **str** | usage_stat when filled from UsageStat | [optional] 

## Example

```python
from mudbase.models.monitoring_performance_response_metrics import MonitoringPerformanceResponseMetrics

# TODO update the JSON string below
json = "{}"
# create an instance of MonitoringPerformanceResponseMetrics from a JSON string
monitoring_performance_response_metrics_instance = MonitoringPerformanceResponseMetrics.from_json(json)
# print the JSON string representation of the object
print(MonitoringPerformanceResponseMetrics.to_json())

# convert the object into a dict
monitoring_performance_response_metrics_dict = monitoring_performance_response_metrics_instance.to_dict()
# create an instance of MonitoringPerformanceResponseMetrics from a dict
monitoring_performance_response_metrics_from_dict = MonitoringPerformanceResponseMetrics.from_dict(monitoring_performance_response_metrics_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


