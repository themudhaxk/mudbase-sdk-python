# ProjectUsageResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**usage** | [**ProjectUsage**](ProjectUsage.md) |  | [optional] 
**limits** | [**Limits**](Limits.md) |  | [optional] 

## Example

```python
from mudbase.models.project_usage_response import ProjectUsageResponse

# TODO update the JSON string below
json = "{}"
# create an instance of ProjectUsageResponse from a JSON string
project_usage_response_instance = ProjectUsageResponse.from_json(json)
# print the JSON string representation of the object
print(ProjectUsageResponse.to_json())

# convert the object into a dict
project_usage_response_dict = project_usage_response_instance.to_dict()
# create an instance of ProjectUsageResponse from a dict
project_usage_response_from_dict = ProjectUsageResponse.from_dict(project_usage_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


