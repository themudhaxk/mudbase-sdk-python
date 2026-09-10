# DashboardOverviewDataRequestVolume14dInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**var_date** | **str** |  | [optional] 
**api_calls** | **int** |  | [optional] 
**latency_tracked** | **int** | Middleware-metered responses that day (UsageStat latencyCount) | [optional] 

## Example

```python
from mudbase.models.dashboard_overview_data_request_volume14d_inner import DashboardOverviewDataRequestVolume14dInner

# TODO update the JSON string below
json = "{}"
# create an instance of DashboardOverviewDataRequestVolume14dInner from a JSON string
dashboard_overview_data_request_volume14d_inner_instance = DashboardOverviewDataRequestVolume14dInner.from_json(json)
# print the JSON string representation of the object
print(DashboardOverviewDataRequestVolume14dInner.to_json())

# convert the object into a dict
dashboard_overview_data_request_volume14d_inner_dict = dashboard_overview_data_request_volume14d_inner_instance.to_dict()
# create an instance of DashboardOverviewDataRequestVolume14dInner from a dict
dashboard_overview_data_request_volume14d_inner_from_dict = DashboardOverviewDataRequestVolume14dInner.from_dict(dashboard_overview_data_request_volume14d_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


