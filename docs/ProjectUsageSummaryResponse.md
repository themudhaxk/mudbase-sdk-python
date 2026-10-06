# ProjectUsageSummaryResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**success** | **bool** |  | [optional] 
**data** | **object** | Contains requests, activeUsers, requestVolume14d, latency, platformUptimePct30d, platformUptimeSamples | [optional] 

## Example

```python
from mudbase.models.project_usage_summary_response import ProjectUsageSummaryResponse

# TODO update the JSON string below
json = "{}"
# create an instance of ProjectUsageSummaryResponse from a JSON string
project_usage_summary_response_instance = ProjectUsageSummaryResponse.from_json(json)
# print the JSON string representation of the object
print(ProjectUsageSummaryResponse.to_json())

# convert the object into a dict
project_usage_summary_response_dict = project_usage_summary_response_instance.to_dict()
# create an instance of ProjectUsageSummaryResponse from a dict
project_usage_summary_response_from_dict = ProjectUsageSummaryResponse.from_dict(project_usage_summary_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


