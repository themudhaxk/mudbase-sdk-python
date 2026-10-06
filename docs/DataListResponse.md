# DataListResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**data** | [**List[DataListResponseDataInner]**](DataListResponseDataInner.md) |  | [optional] 
**pagination** | [**Pagination**](Pagination.md) |  | [optional] 

## Example

```python
from mudbase.models.data_list_response import DataListResponse

# TODO update the JSON string below
json = "{}"
# create an instance of DataListResponse from a JSON string
data_list_response_instance = DataListResponse.from_json(json)
# print the JSON string representation of the object
print(DataListResponse.to_json())

# convert the object into a dict
data_list_response_dict = data_list_response_instance.to_dict()
# create an instance of DataListResponse from a dict
data_list_response_from_dict = DataListResponse.from_dict(data_list_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


