# GetUsageStats200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**stats** | [**GetUsageStats200ResponseStats**](GetUsageStats200ResponseStats.md) |  | [optional] 

## Example

```python
from mudbase.models.get_usage_stats200_response import GetUsageStats200Response

# TODO update the JSON string below
json = "{}"
# create an instance of GetUsageStats200Response from a JSON string
get_usage_stats200_response_instance = GetUsageStats200Response.from_json(json)
# print the JSON string representation of the object
print(GetUsageStats200Response.to_json())

# convert the object into a dict
get_usage_stats200_response_dict = get_usage_stats200_response_instance.to_dict()
# create an instance of GetUsageStats200Response from a dict
get_usage_stats200_response_from_dict = GetUsageStats200Response.from_dict(get_usage_stats200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


