# RestoreBackup200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**message** | **str** |  | [optional] 
**restore** | [**RestoreBackup200ResponseRestore**](RestoreBackup200ResponseRestore.md) |  | [optional] 

## Example

```python
from mudbase.models.restore_backup200_response import RestoreBackup200Response

# TODO update the JSON string below
json = "{}"
# create an instance of RestoreBackup200Response from a JSON string
restore_backup200_response_instance = RestoreBackup200Response.from_json(json)
# print the JSON string representation of the object
print(RestoreBackup200Response.to_json())

# convert the object into a dict
restore_backup200_response_dict = restore_backup200_response_instance.to_dict()
# create an instance of RestoreBackup200Response from a dict
restore_backup200_response_from_dict = RestoreBackup200Response.from_dict(restore_backup200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


