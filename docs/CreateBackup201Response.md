# CreateBackup201Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**backup** | [**CreateBackup201ResponseBackup**](CreateBackup201ResponseBackup.md) |  | [optional] 

## Example

```python
from mudbase.models.create_backup201_response import CreateBackup201Response

# TODO update the JSON string below
json = "{}"
# create an instance of CreateBackup201Response from a JSON string
create_backup201_response_instance = CreateBackup201Response.from_json(json)
# print the JSON string representation of the object
print(CreateBackup201Response.to_json())

# convert the object into a dict
create_backup201_response_dict = create_backup201_response_instance.to_dict()
# create an instance of CreateBackup201Response from a dict
create_backup201_response_from_dict = CreateBackup201Response.from_dict(create_backup201_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


