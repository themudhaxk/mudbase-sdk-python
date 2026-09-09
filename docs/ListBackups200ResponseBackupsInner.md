# ListBackups200ResponseBackupsInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** |  | [optional] 
**description** | **str** |  | [optional] 
**status** | **str** |  | [optional] 
**size** | **int** |  | [optional] 
**collections** | **List[str]** |  | [optional] 
**file_count** | **int** |  | [optional] 
**created_at** | **datetime** |  | [optional] 
**completed_at** | **datetime** |  | [optional] 

## Example

```python
from mudbase.models.list_backups200_response_backups_inner import ListBackups200ResponseBackupsInner

# TODO update the JSON string below
json = "{}"
# create an instance of ListBackups200ResponseBackupsInner from a JSON string
list_backups200_response_backups_inner_instance = ListBackups200ResponseBackupsInner.from_json(json)
# print the JSON string representation of the object
print(ListBackups200ResponseBackupsInner.to_json())

# convert the object into a dict
list_backups200_response_backups_inner_dict = list_backups200_response_backups_inner_instance.to_dict()
# create an instance of ListBackups200ResponseBackupsInner from a dict
list_backups200_response_backups_inner_from_dict = ListBackups200ResponseBackupsInner.from_dict(list_backups200_response_backups_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


