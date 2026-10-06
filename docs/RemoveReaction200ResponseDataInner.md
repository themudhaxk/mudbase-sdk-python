# RemoveReaction200ResponseDataInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**emoji** | **str** |  | [optional] 
**count** | **int** |  | [optional] 
**users** | **List[str]** |  | [optional] 

## Example

```python
from mudbase.models.remove_reaction200_response_data_inner import RemoveReaction200ResponseDataInner

# TODO update the JSON string below
json = "{}"
# create an instance of RemoveReaction200ResponseDataInner from a JSON string
remove_reaction200_response_data_inner_instance = RemoveReaction200ResponseDataInner.from_json(json)
# print the JSON string representation of the object
print(RemoveReaction200ResponseDataInner.to_json())

# convert the object into a dict
remove_reaction200_response_data_inner_dict = remove_reaction200_response_data_inner_instance.to_dict()
# create an instance of RemoveReaction200ResponseDataInner from a dict
remove_reaction200_response_data_inner_from_dict = RemoveReaction200ResponseDataInner.from_dict(remove_reaction200_response_data_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


