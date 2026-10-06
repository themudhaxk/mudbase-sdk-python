# Limits


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**projects** | **int** |  | [optional] 
**users** | **int** |  | [optional] 
**storage** | **int** |  | [optional] 
**bandwidth** | **int** |  | [optional] 
**api_calls** | **int** |  | [optional] 
**db_reads** | **int** |  | [optional] 
**db_writes** | **int** |  | [optional] 

## Example

```python
from mudbase.models.limits import Limits

# TODO update the JSON string below
json = "{}"
# create an instance of Limits from a JSON string
limits_instance = Limits.from_json(json)
# print the JSON string representation of the object
print(Limits.to_json())

# convert the object into a dict
limits_dict = limits_instance.to_dict()
# create an instance of Limits from a dict
limits_from_dict = Limits.from_dict(limits_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


