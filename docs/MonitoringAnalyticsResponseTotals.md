# MonitoringAnalyticsResponseTotals


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**total_api_calls** | **int** |  | [optional] 
**total_db_reads** | **int** |  | [optional] 
**total_db_writes** | **int** |  | [optional] 
**total_storage** | **int** |  | [optional] 
**total_bandwidth** | **int** |  | [optional] 

## Example

```python
from mudbase.models.monitoring_analytics_response_totals import MonitoringAnalyticsResponseTotals

# TODO update the JSON string below
json = "{}"
# create an instance of MonitoringAnalyticsResponseTotals from a JSON string
monitoring_analytics_response_totals_instance = MonitoringAnalyticsResponseTotals.from_json(json)
# print the JSON string representation of the object
print(MonitoringAnalyticsResponseTotals.to_json())

# convert the object into a dict
monitoring_analytics_response_totals_dict = monitoring_analytics_response_totals_instance.to_dict()
# create an instance of MonitoringAnalyticsResponseTotals from a dict
monitoring_analytics_response_totals_from_dict = MonitoringAnalyticsResponseTotals.from_dict(monitoring_analytics_response_totals_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


