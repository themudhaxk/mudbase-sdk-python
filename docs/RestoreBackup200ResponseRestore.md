# RestoreBackup200ResponseRestore


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** |  | [optional] 
**status** | **str** |  | [optional] 
**restore_mode** | **str** |  | [optional] 
**started_at** | **datetime** |  | [optional] 
**estimated_completion** | **datetime** |  | [optional] 

## Example

```python
from mudbase.models.restore_backup200_response_restore import RestoreBackup200ResponseRestore

# TODO update the JSON string below
json = "{}"
# create an instance of RestoreBackup200ResponseRestore from a JSON string
restore_backup200_response_restore_instance = RestoreBackup200ResponseRestore.from_json(json)
# print the JSON string representation of the object
print(RestoreBackup200ResponseRestore.to_json())

# convert the object into a dict
restore_backup200_response_restore_dict = restore_backup200_response_restore_instance.to_dict()
# create an instance of RestoreBackup200ResponseRestore from a dict
restore_backup200_response_restore_from_dict = RestoreBackup200ResponseRestore.from_dict(restore_backup200_response_restore_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


