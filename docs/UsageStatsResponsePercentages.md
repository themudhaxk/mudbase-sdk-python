# UsageStatsResponsePercentages


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**api_calls** | **float** |  | [optional] 
**storage** | **float** |  | [optional] 
**bandwidth** | **float** |  | [optional] 

## Example

```python
from mudbase.models.usage_stats_response_percentages import UsageStatsResponsePercentages

# TODO update the JSON string below
json = "{}"
# create an instance of UsageStatsResponsePercentages from a JSON string
usage_stats_response_percentages_instance = UsageStatsResponsePercentages.from_json(json)
# print the JSON string representation of the object
print(UsageStatsResponsePercentages.to_json())

# convert the object into a dict
usage_stats_response_percentages_dict = usage_stats_response_percentages_instance.to_dict()
# create an instance of UsageStatsResponsePercentages from a dict
usage_stats_response_percentages_from_dict = UsageStatsResponsePercentages.from_dict(usage_stats_response_percentages_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


