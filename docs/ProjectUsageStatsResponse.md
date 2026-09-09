# ProjectUsageStatsResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**project** | [**ProjectUsageStatsResponseProject**](ProjectUsageStatsResponseProject.md) |  | [optional] 
**usage** | [**ProjectUsage**](ProjectUsage.md) |  | [optional] 
**period** | **str** |  | [optional] 

## Example

```python
from mudbase.models.project_usage_stats_response import ProjectUsageStatsResponse

# TODO update the JSON string below
json = "{}"
# create an instance of ProjectUsageStatsResponse from a JSON string
project_usage_stats_response_instance = ProjectUsageStatsResponse.from_json(json)
# print the JSON string representation of the object
print(ProjectUsageStatsResponse.to_json())

# convert the object into a dict
project_usage_stats_response_dict = project_usage_stats_response_instance.to_dict()
# create an instance of ProjectUsageStatsResponse from a dict
project_usage_stats_response_from_dict = ProjectUsageStatsResponse.from_dict(project_usage_stats_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


