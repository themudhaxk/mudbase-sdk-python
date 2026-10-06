# DashboardOverviewData


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**project** | [**DashboardOverviewDataProject**](DashboardOverviewDataProject.md) |  | [optional] 
**requests** | [**DashboardOverviewDataRequests**](DashboardOverviewDataRequests.md) |  | [optional] 
**active_users** | [**DashboardOverviewDataActiveUsers**](DashboardOverviewDataActiveUsers.md) |  | [optional] 
**latency** | [**DashboardOverviewDataLatency**](DashboardOverviewDataLatency.md) |  | [optional] 
**uptime** | [**DashboardOverviewDataUptime**](DashboardOverviewDataUptime.md) |  | [optional] 
**request_volume14d** | [**List[DashboardOverviewDataRequestVolume14dInner]**](DashboardOverviewDataRequestVolume14dInner.md) |  | [optional] 
**recent_activity** | [**List[DashboardActivityItem]**](DashboardActivityItem.md) |  | [optional] 
**generated_at** | **datetime** |  | [optional] 

## Example

```python
from mudbase.models.dashboard_overview_data import DashboardOverviewData

# TODO update the JSON string below
json = "{}"
# create an instance of DashboardOverviewData from a JSON string
dashboard_overview_data_instance = DashboardOverviewData.from_json(json)
# print the JSON string representation of the object
print(DashboardOverviewData.to_json())

# convert the object into a dict
dashboard_overview_data_dict = dashboard_overview_data_instance.to_dict()
# create an instance of DashboardOverviewData from a dict
dashboard_overview_data_from_dict = DashboardOverviewData.from_dict(dashboard_overview_data_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


