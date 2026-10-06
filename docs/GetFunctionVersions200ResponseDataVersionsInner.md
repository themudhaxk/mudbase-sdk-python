# GetFunctionVersions200ResponseDataVersionsInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** |  | [optional] 
**code** | **str** |  | [optional] 
**version** | **int** |  | [optional] 
**created_at** | **datetime** |  | [optional] 
**created_by** | **str** |  | [optional] 
**comment** | **str** |  | [optional] 

## Example

```python
from mudbase.models.get_function_versions200_response_data_versions_inner import GetFunctionVersions200ResponseDataVersionsInner

# TODO update the JSON string below
json = "{}"
# create an instance of GetFunctionVersions200ResponseDataVersionsInner from a JSON string
get_function_versions200_response_data_versions_inner_instance = GetFunctionVersions200ResponseDataVersionsInner.from_json(json)
# print the JSON string representation of the object
print(GetFunctionVersions200ResponseDataVersionsInner.to_json())

# convert the object into a dict
get_function_versions200_response_data_versions_inner_dict = get_function_versions200_response_data_versions_inner_instance.to_dict()
# create an instance of GetFunctionVersions200ResponseDataVersionsInner from a dict
get_function_versions200_response_data_versions_inner_from_dict = GetFunctionVersions200ResponseDataVersionsInner.from_dict(get_function_versions200_response_data_versions_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


