# DashboardOverviewDataUptime

Organization-wide uptime KPI; platformProbe* is infra (Mongo); projectHttp* is this project only for comparison.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**scope** | **str** |  | [optional] 
**display_pct30d** | **float** |  | [optional] 
**display_source** | **str** |  | [optional] 
**is_preliminary** | **bool** |  | [optional] 
**platform_probe_pct30d** | **float** |  | [optional] 
**platform_samples** | **int** |  | [optional] 
**platform_ok_samples** | **int** |  | [optional] 
**org_http_non5xx_pct30d** | **float** |  | [optional] 
**org_http_sampled30d** | **int** |  | [optional] 
**org_http5xx30d** | **int** | Metered 5xx count from UsageStat (trackApiCall) | [optional] 
**project_http5xx30d** | **int** | This project’s metered 5xx count (30d) | [optional] 
**global_http_non5xx_pct30d** | **float** | Deprecated alias for orgHttpNon5xxPct30d | [optional] 
**global_http_sampled30d** | **int** | Deprecated alias for orgHttpSampled30d | [optional] 
**request_non5xx_pct30d** | **float** | Deprecated alias for orgHttpNon5xxPct30d | [optional] 
**request_sampled30d** | **int** | Deprecated alias for orgHttpSampled30d | [optional] 
**project_http_non5xx_pct30d** | **float** |  | [optional] 
**project_http_sampled30d** | **int** |  | [optional] 
**help** | **str** |  | [optional] 

## Example

```python
from mudbase.models.dashboard_overview_data_uptime import DashboardOverviewDataUptime

# TODO update the JSON string below
json = "{}"
# create an instance of DashboardOverviewDataUptime from a JSON string
dashboard_overview_data_uptime_instance = DashboardOverviewDataUptime.from_json(json)
# print the JSON string representation of the object
print(DashboardOverviewDataUptime.to_json())

# convert the object into a dict
dashboard_overview_data_uptime_dict = dashboard_overview_data_uptime_instance.to_dict()
# create an instance of DashboardOverviewDataUptime from a dict
dashboard_overview_data_uptime_from_dict = DashboardOverviewDataUptime.from_dict(dashboard_overview_data_uptime_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


