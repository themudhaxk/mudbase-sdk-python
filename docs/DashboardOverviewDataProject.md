# DashboardOverviewDataProject


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** |  | [optional] 
**name** | **str** |  | [optional] 
**slug** | **str** |  | [optional] 

## Example

```python
from mudbase.models.dashboard_overview_data_project import DashboardOverviewDataProject

# TODO update the JSON string below
json = "{}"
# create an instance of DashboardOverviewDataProject from a JSON string
dashboard_overview_data_project_instance = DashboardOverviewDataProject.from_json(json)
# print the JSON string representation of the object
print(DashboardOverviewDataProject.to_json())

# convert the object into a dict
dashboard_overview_data_project_dict = dashboard_overview_data_project_instance.to_dict()
# create an instance of DashboardOverviewDataProject from a dict
dashboard_overview_data_project_from_dict = DashboardOverviewDataProject.from_dict(dashboard_overview_data_project_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


