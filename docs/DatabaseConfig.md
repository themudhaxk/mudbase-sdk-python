# DatabaseConfig


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**collections** | **List[str]** |  | [optional] 

## Example

```python
from mudbase.models.database_config import DatabaseConfig

# TODO update the JSON string below
json = "{}"
# create an instance of DatabaseConfig from a JSON string
database_config_instance = DatabaseConfig.from_json(json)
# print the JSON string representation of the object
print(DatabaseConfig.to_json())

# convert the object into a dict
database_config_dict = database_config_instance.to_dict()
# create an instance of DatabaseConfig from a dict
database_config_from_dict = DatabaseConfig.from_dict(database_config_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


