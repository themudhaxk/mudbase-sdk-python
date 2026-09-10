# Project


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** |  | [optional] 
**name** | **str** |  | [optional] 
**description** | **str** |  | [optional] 
**slug** | **str** |  | [optional] 
**org** | **str** |  | [optional] 
**auth** | [**AuthConfig**](AuthConfig.md) |  | [optional] 
**database** | [**DatabaseConfig**](DatabaseConfig.md) |  | [optional] 
**storage** | [**StorageConfig**](StorageConfig.md) |  | [optional] 
**settings** | [**ProjectSettings**](ProjectSettings.md) |  | [optional] 
**usage** | [**ProjectUsage**](ProjectUsage.md) |  | [optional] 
**created_at** | **datetime** |  | [optional] 
**updated_at** | **datetime** |  | [optional] 

## Example

```python
from mudbase.models.project import Project

# TODO update the JSON string below
json = "{}"
# create an instance of Project from a JSON string
project_instance = Project.from_json(json)
# print the JSON string representation of the object
print(Project.to_json())

# convert the object into a dict
project_dict = project_instance.to_dict()
# create an instance of Project from a dict
project_from_dict = Project.from_dict(project_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


