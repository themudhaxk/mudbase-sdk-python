# CreateBackupRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**description** | **str** |  | [optional] 
**include_files** | **bool** |  | [optional] [default to True]
**include_wallets** | **bool** |  | [optional] [default to False]

## Example

```python
from mudbase.models.create_backup_request import CreateBackupRequest

# TODO update the JSON string below
json = "{}"
# create an instance of CreateBackupRequest from a JSON string
create_backup_request_instance = CreateBackupRequest.from_json(json)
# print the JSON string representation of the object
print(CreateBackupRequest.to_json())

# convert the object into a dict
create_backup_request_dict = create_backup_request_instance.to_dict()
# create an instance of CreateBackupRequest from a dict
create_backup_request_from_dict = CreateBackupRequest.from_dict(create_backup_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


