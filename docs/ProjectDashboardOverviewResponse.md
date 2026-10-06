# ProjectDashboardOverviewResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**success** | **bool** |  | 
**data** | [**DashboardOverviewData**](DashboardOverviewData.md) |  | 

## Example

```python
from mudbase.models.project_dashboard_overview_response import ProjectDashboardOverviewResponse

# TODO update the JSON string below
json = "{}"
# create an instance of ProjectDashboardOverviewResponse from a JSON string
project_dashboard_overview_response_instance = ProjectDashboardOverviewResponse.from_json(json)
# print the JSON string representation of the object
print(ProjectDashboardOverviewResponse.to_json())

# convert the object into a dict
project_dashboard_overview_response_dict = project_dashboard_overview_response_instance.to_dict()
# create an instance of ProjectDashboardOverviewResponse from a dict
project_dashboard_overview_response_from_dict = ProjectDashboardOverviewResponse.from_dict(project_dashboard_overview_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


