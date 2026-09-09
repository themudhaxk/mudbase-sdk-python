# GetSearchAnalytics200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**total_searches** | **int** |  | [optional] 
**top_queries** | [**List[GetSearchAnalytics200ResponseTopQueriesInner]**](GetSearchAnalytics200ResponseTopQueriesInner.md) |  | [optional] 
**searches_by_collection** | **object** |  | [optional] 
**average_response_time** | **float** |  | [optional] 

## Example

```python
from mudbase.models.get_search_analytics200_response import GetSearchAnalytics200Response

# TODO update the JSON string below
json = "{}"
# create an instance of GetSearchAnalytics200Response from a JSON string
get_search_analytics200_response_instance = GetSearchAnalytics200Response.from_json(json)
# print the JSON string representation of the object
print(GetSearchAnalytics200Response.to_json())

# convert the object into a dict
get_search_analytics200_response_dict = get_search_analytics200_response_instance.to_dict()
# create an instance of GetSearchAnalytics200Response from a dict
get_search_analytics200_response_from_dict = GetSearchAnalytics200Response.from_dict(get_search_analytics200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


