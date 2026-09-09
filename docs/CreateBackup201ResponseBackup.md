# CreateBackup201ResponseBackup


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** |  | [optional] 
**project** | **str** |  | [optional] 
**description** | **str** |  | [optional] 
**status** | **str** |  | [optional] 
**size** | **int** |  | [optional] 
**collections** | **List[str]** |  | [optional] 
**created_at** | **datetime** |  | [optional] 
**estimated_completion** | **datetime** |  | [optional] 

## Example

```python
from mudbase.models.create_backup201_response_backup import CreateBackup201ResponseBackup

# TODO update the JSON string below
json = "{}"
# create an instance of CreateBackup201ResponseBackup from a JSON string
create_backup201_response_backup_instance = CreateBackup201ResponseBackup.from_json(json)
# print the JSON string representation of the object
print(CreateBackup201ResponseBackup.to_json())

# convert the object into a dict
create_backup201_response_backup_dict = create_backup201_response_backup_instance.to_dict()
# create an instance of CreateBackup201ResponseBackup from a dict
create_backup201_response_backup_from_dict = CreateBackup201ResponseBackup.from_dict(create_backup201_response_backup_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


