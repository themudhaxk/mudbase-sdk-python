# DashboardOverviewDataRequests


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**today** | **int** | Billing trackApiCall count (UTC day) | [optional] 
**yesterday** | **int** |  | [optional] 
**latency_tracked_today** | **int** | UsageStat latencyCount for this project (middleware-metered responses) | [optional] 
**latency_tracked_yesterday** | **int** |  | [optional] 
**metering_note** | **str** |  | [optional] 
**change_pct** | **float** |  | [optional] 
**direction** | **str** |  | [optional] 

## Example

```python
from mudbase.models.dashboard_overview_data_requests import DashboardOverviewDataRequests

# TODO update the JSON string below
json = "{}"
# create an instance of DashboardOverviewDataRequests from a JSON string
dashboard_overview_data_requests_instance = DashboardOverviewDataRequests.from_json(json)
# print the JSON string representation of the object
print(DashboardOverviewDataRequests.to_json())

# convert the object into a dict
dashboard_overview_data_requests_dict = dashboard_overview_data_requests_instance.to_dict()
# create an instance of DashboardOverviewDataRequests from a dict
dashboard_overview_data_requests_from_dict = DashboardOverviewDataRequests.from_dict(dashboard_overview_data_requests_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


