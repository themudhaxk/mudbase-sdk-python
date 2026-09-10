# GetGlobalAnalytics200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**active_connections** | **int** |  | [optional] 
**peak_connections** | **int** |  | [optional] 
**total_events** | **int** |  | [optional] 
**events_per_minute** | **int** |  | [optional] 

## Example

```python
from mudbase.models.get_global_analytics200_response import GetGlobalAnalytics200Response

# TODO update the JSON string below
json = "{}"
# create an instance of GetGlobalAnalytics200Response from a JSON string
get_global_analytics200_response_instance = GetGlobalAnalytics200Response.from_json(json)
# print the JSON string representation of the object
print(GetGlobalAnalytics200Response.to_json())

# convert the object into a dict
get_global_analytics200_response_dict = get_global_analytics200_response_instance.to_dict()
# create an instance of GetGlobalAnalytics200Response from a dict
get_global_analytics200_response_from_dict = GetGlobalAnalytics200Response.from_dict(get_global_analytics200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


