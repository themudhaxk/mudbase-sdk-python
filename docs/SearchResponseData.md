# SearchResponseData


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**results** | [**List[SearchResult]**](SearchResult.md) |  | [optional] 
**pagination** | [**Pagination**](Pagination.md) |  | [optional] 
**query** | **str** |  | [optional] 
**search_time** | **int** |  | [optional] 

## Example

```python
from mudbase.models.search_response_data import SearchResponseData

# TODO update the JSON string below
json = "{}"
# create an instance of SearchResponseData from a JSON string
search_response_data_instance = SearchResponseData.from_json(json)
# print the JSON string representation of the object
print(SearchResponseData.to_json())

# convert the object into a dict
search_response_data_dict = search_response_data_instance.to_dict()
# create an instance of SearchResponseData from a dict
search_response_data_from_dict = SearchResponseData.from_dict(search_response_data_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


