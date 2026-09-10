# GetUsageWarnings200ResponseWarningsInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**resource** | **str** |  | [optional] 
**threshold** | **float** |  | [optional] 
**current** | **float** |  | [optional] 
**limit** | **float** |  | [optional] 
**message** | **str** |  | [optional] 

## Example

```python
from mudbase.models.get_usage_warnings200_response_warnings_inner import GetUsageWarnings200ResponseWarningsInner

# TODO update the JSON string below
json = "{}"
# create an instance of GetUsageWarnings200ResponseWarningsInner from a JSON string
get_usage_warnings200_response_warnings_inner_instance = GetUsageWarnings200ResponseWarningsInner.from_json(json)
# print the JSON string representation of the object
print(GetUsageWarnings200ResponseWarningsInner.to_json())

# convert the object into a dict
get_usage_warnings200_response_warnings_inner_dict = get_usage_warnings200_response_warnings_inner_instance.to_dict()
# create an instance of GetUsageWarnings200ResponseWarningsInner from a dict
get_usage_warnings200_response_warnings_inner_from_dict = GetUsageWarnings200ResponseWarningsInner.from_dict(get_usage_warnings200_response_warnings_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


