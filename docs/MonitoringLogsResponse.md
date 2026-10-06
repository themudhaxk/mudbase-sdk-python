# MonitoringLogsResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**logs** | [**List[MonitoringLogsResponseLogsInner]**](MonitoringLogsResponseLogsInner.md) |  | [optional] 
**count** | **int** |  | [optional] 
**page** | **int** |  | [optional] 
**limit** | **int** |  | [optional] 
**total** | **int** |  | [optional] 
**total_pages** | **int** |  | [optional] 

## Example

```python
from mudbase.models.monitoring_logs_response import MonitoringLogsResponse

# TODO update the JSON string below
json = "{}"
# create an instance of MonitoringLogsResponse from a JSON string
monitoring_logs_response_instance = MonitoringLogsResponse.from_json(json)
# print the JSON string representation of the object
print(MonitoringLogsResponse.to_json())

# convert the object into a dict
monitoring_logs_response_dict = monitoring_logs_response_instance.to_dict()
# create an instance of MonitoringLogsResponse from a dict
monitoring_logs_response_from_dict = MonitoringLogsResponse.from_dict(monitoring_logs_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


