# GetUserOverview200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**user** | **object** | User profile (metadata only) | [optional] 
**footprint** | [**GetUserOverview200ResponseFootprint**](GetUserOverview200ResponseFootprint.md) |  | [optional] 

## Example

```python
from mudbase.models.get_user_overview200_response import GetUserOverview200Response

# TODO update the JSON string below
json = "{}"
# create an instance of GetUserOverview200Response from a JSON string
get_user_overview200_response_instance = GetUserOverview200Response.from_json(json)
# print the JSON string representation of the object
print(GetUserOverview200Response.to_json())

# convert the object into a dict
get_user_overview200_response_dict = get_user_overview200_response_instance.to_dict()
# create an instance of GetUserOverview200Response from a dict
get_user_overview200_response_from_dict = GetUserOverview200Response.from_dict(get_user_overview200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


