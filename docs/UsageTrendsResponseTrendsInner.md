# UsageTrendsResponseTrendsInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | [**UsageTrendsResponseTrendsInnerId**](UsageTrendsResponseTrendsInnerId.md) |  | [optional] 
**api_calls** | **int** |  | [optional] 
**storage** | **int** |  | [optional] 
**bandwidth** | **int** |  | [optional] 
**db_reads** | **int** |  | [optional] 
**db_writes** | **int** |  | [optional] 

## Example

```python
from mudbase.models.usage_trends_response_trends_inner import UsageTrendsResponseTrendsInner

# TODO update the JSON string below
json = "{}"
# create an instance of UsageTrendsResponseTrendsInner from a JSON string
usage_trends_response_trends_inner_instance = UsageTrendsResponseTrendsInner.from_json(json)
# print the JSON string representation of the object
print(UsageTrendsResponseTrendsInner.to_json())

# convert the object into a dict
usage_trends_response_trends_inner_dict = usage_trends_response_trends_inner_instance.to_dict()
# create an instance of UsageTrendsResponseTrendsInner from a dict
usage_trends_response_trends_inner_from_dict = UsageTrendsResponseTrendsInner.from_dict(usage_trends_response_trends_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


