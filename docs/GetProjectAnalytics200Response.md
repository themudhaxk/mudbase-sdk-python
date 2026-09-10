# GetProjectAnalytics200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**project_id** | **str** |  | [optional] 
**active_connections** | **int** |  | [optional] 
**total_events** | **int** |  | [optional] 
**last_activity** | **datetime** |  | [optional] 
**timestamp** | **datetime** |  | [optional] 

## Example

```python
from mudbase.models.get_project_analytics200_response import GetProjectAnalytics200Response

# TODO update the JSON string below
json = "{}"
# create an instance of GetProjectAnalytics200Response from a JSON string
get_project_analytics200_response_instance = GetProjectAnalytics200Response.from_json(json)
# print the JSON string representation of the object
print(GetProjectAnalytics200Response.to_json())

# convert the object into a dict
get_project_analytics200_response_dict = get_project_analytics200_response_instance.to_dict()
# create an instance of GetProjectAnalytics200Response from a dict
get_project_analytics200_response_from_dict = GetProjectAnalytics200Response.from_dict(get_project_analytics200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


