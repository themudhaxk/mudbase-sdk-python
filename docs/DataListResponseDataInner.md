# DataListResponseDataInner

Document from the collection (includes _id, createdAt, updatedAt, and all collection fields). Additional fields are defined in the collection schema.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** | Document ID (MongoDB ObjectId) - use this as documentId in API calls | [optional] 
**created_at** | **datetime** | Document creation timestamp | [optional] 
**updated_at** | **datetime** | Document last update timestamp | [optional] 

## Example

```python
from mudbase.models.data_list_response_data_inner import DataListResponseDataInner

# TODO update the JSON string below
json = "{}"
# create an instance of DataListResponseDataInner from a JSON string
data_list_response_data_inner_instance = DataListResponseDataInner.from_json(json)
# print the JSON string representation of the object
print(DataListResponseDataInner.to_json())

# convert the object into a dict
data_list_response_data_inner_dict = data_list_response_data_inner_instance.to_dict()
# create an instance of DataListResponseDataInner from a dict
data_list_response_data_inner_from_dict = DataListResponseDataInner.from_dict(data_list_response_data_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


