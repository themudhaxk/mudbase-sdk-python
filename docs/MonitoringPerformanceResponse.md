# MonitoringPerformanceResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**period** | **str** |  | [optional] 
**metrics** | [**MonitoringPerformanceResponseMetrics**](MonitoringPerformanceResponseMetrics.md) |  | [optional] 
**top_endpoints** | **List[object]** |  | [optional] 

## Example

```python
from mudbase.models.monitoring_performance_response import MonitoringPerformanceResponse

# TODO update the JSON string below
json = "{}"
# create an instance of MonitoringPerformanceResponse from a JSON string
monitoring_performance_response_instance = MonitoringPerformanceResponse.from_json(json)
# print the JSON string representation of the object
print(MonitoringPerformanceResponse.to_json())

# convert the object into a dict
monitoring_performance_response_dict = monitoring_performance_response_instance.to_dict()
# create an instance of MonitoringPerformanceResponse from a dict
monitoring_performance_response_from_dict = MonitoringPerformanceResponse.from_dict(monitoring_performance_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


