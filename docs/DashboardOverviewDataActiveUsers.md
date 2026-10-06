# DashboardOverviewDataActiveUsers


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**last24h** | **int** |  | [optional] 
**last7d** | **int** |  | [optional] 
**last30d** | **int** |  | [optional] 
**change_pct7d** | **float** |  | [optional] 
**direction7d** | **str** |  | [optional] 
**realtime_connected** | **int** |  | [optional] 

## Example

```python
from mudbase.models.dashboard_overview_data_active_users import DashboardOverviewDataActiveUsers

# TODO update the JSON string below
json = "{}"
# create an instance of DashboardOverviewDataActiveUsers from a JSON string
dashboard_overview_data_active_users_instance = DashboardOverviewDataActiveUsers.from_json(json)
# print the JSON string representation of the object
print(DashboardOverviewDataActiveUsers.to_json())

# convert the object into a dict
dashboard_overview_data_active_users_dict = dashboard_overview_data_active_users_instance.to_dict()
# create an instance of DashboardOverviewDataActiveUsers from a dict
dashboard_overview_data_active_users_from_dict = DashboardOverviewDataActiveUsers.from_dict(dashboard_overview_data_active_users_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


