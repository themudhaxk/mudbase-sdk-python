# UsageStatsResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**usage** | [**Usage**](Usage.md) |  | [optional] 
**limits** | [**Limits**](Limits.md) |  | [optional] 
**plan** | [**Plan**](Plan.md) |  | [optional] 
**period** | **str** |  | [optional] 
**percentages** | [**UsageStatsResponsePercentages**](UsageStatsResponsePercentages.md) |  | [optional] 

## Example

```python
from mudbase.models.usage_stats_response import UsageStatsResponse

# TODO update the JSON string below
json = "{}"
# create an instance of UsageStatsResponse from a JSON string
usage_stats_response_instance = UsageStatsResponse.from_json(json)
# print the JSON string representation of the object
print(UsageStatsResponse.to_json())

# convert the object into a dict
usage_stats_response_dict = usage_stats_response_instance.to_dict()
# create an instance of UsageStatsResponse from a dict
usage_stats_response_from_dict = UsageStatsResponse.from_dict(usage_stats_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


