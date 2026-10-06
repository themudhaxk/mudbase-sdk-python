# GetUsageStats200ResponseStats


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**total_calls** | **int** |  | [optional] 
**success_calls** | **int** |  | [optional] 
**failed_calls** | **int** |  | [optional] 

## Example

```python
from mudbase.models.get_usage_stats200_response_stats import GetUsageStats200ResponseStats

# TODO update the JSON string below
json = "{}"
# create an instance of GetUsageStats200ResponseStats from a JSON string
get_usage_stats200_response_stats_instance = GetUsageStats200ResponseStats.from_json(json)
# print the JSON string representation of the object
print(GetUsageStats200ResponseStats.to_json())

# convert the object into a dict
get_usage_stats200_response_stats_dict = get_usage_stats200_response_stats_instance.to_dict()
# create an instance of GetUsageStats200ResponseStats from a dict
get_usage_stats200_response_stats_from_dict = GetUsageStats200ResponseStats.from_dict(get_usage_stats200_response_stats_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


