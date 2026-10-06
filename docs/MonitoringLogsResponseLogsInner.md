# MonitoringLogsResponseLogsInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** |  | [optional] 
**timestamp** | **datetime** |  | [optional] 
**level** | **str** |  | [optional] 
**message** | **str** |  | [optional] 
**action** | **str** |  | [optional] 
**activity_title** | **str** |  | [optional] 
**activity_detail** | **str** |  | [optional] 
**user** | [**MonitoringLogsResponseLogsInnerUser**](MonitoringLogsResponseLogsInnerUser.md) |  | [optional] 
**project** | **object** |  | [optional] 
**metadata** | **object** |  | [optional] 

## Example

```python
from mudbase.models.monitoring_logs_response_logs_inner import MonitoringLogsResponseLogsInner

# TODO update the JSON string below
json = "{}"
# create an instance of MonitoringLogsResponseLogsInner from a JSON string
monitoring_logs_response_logs_inner_instance = MonitoringLogsResponseLogsInner.from_json(json)
# print the JSON string representation of the object
print(MonitoringLogsResponseLogsInner.to_json())

# convert the object into a dict
monitoring_logs_response_logs_inner_dict = monitoring_logs_response_logs_inner_instance.to_dict()
# create an instance of MonitoringLogsResponseLogsInner from a dict
monitoring_logs_response_logs_inner_from_dict = MonitoringLogsResponseLogsInner.from_dict(monitoring_logs_response_logs_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


