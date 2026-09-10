# ListBackups200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**backups** | [**List[ListBackups200ResponseBackupsInner]**](ListBackups200ResponseBackupsInner.md) |  | [optional] 
**total** | **int** |  | [optional] 

## Example

```python
from mudbase.models.list_backups200_response import ListBackups200Response

# TODO update the JSON string below
json = "{}"
# create an instance of ListBackups200Response from a JSON string
list_backups200_response_instance = ListBackups200Response.from_json(json)
# print the JSON string representation of the object
print(ListBackups200Response.to_json())

# convert the object into a dict
list_backups200_response_dict = list_backups200_response_instance.to_dict()
# create an instance of ListBackups200Response from a dict
list_backups200_response_from_dict = ListBackups200Response.from_dict(list_backups200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


