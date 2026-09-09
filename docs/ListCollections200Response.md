# ListCollections200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**collections** | [**List[Collection]**](Collection.md) |  | [optional] 
**total** | **int** |  | [optional] 

## Example

```python
from mudbase.models.list_collections200_response import ListCollections200Response

# TODO update the JSON string below
json = "{}"
# create an instance of ListCollections200Response from a JSON string
list_collections200_response_instance = ListCollections200Response.from_json(json)
# print the JSON string representation of the object
print(ListCollections200Response.to_json())

# convert the object into a dict
list_collections200_response_dict = list_collections200_response_instance.to_dict()
# create an instance of ListCollections200Response from a dict
list_collections200_response_from_dict = ListCollections200Response.from_dict(list_collections200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


