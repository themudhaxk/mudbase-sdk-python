# ProjectUsage


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**api_calls** | **int** |  | [optional] 
**storage** | **int** |  | [optional] 
**bandwidth** | **int** |  | [optional] 
**db_reads** | **int** |  | [optional] 
**db_writes** | **int** |  | [optional] 

## Example

```python
from mudbase.models.project_usage import ProjectUsage

# TODO update the JSON string below
json = "{}"
# create an instance of ProjectUsage from a JSON string
project_usage_instance = ProjectUsage.from_json(json)
# print the JSON string representation of the object
print(ProjectUsage.to_json())

# convert the object into a dict
project_usage_dict = project_usage_instance.to_dict()
# create an instance of ProjectUsage from a dict
project_usage_from_dict = ProjectUsage.from_dict(project_usage_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


