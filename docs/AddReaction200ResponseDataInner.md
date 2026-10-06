# AddReaction200ResponseDataInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**emoji** | **str** |  | [optional] 
**users** | **List[str]** |  | [optional] 

## Example

```python
from mudbase.models.add_reaction200_response_data_inner import AddReaction200ResponseDataInner

# TODO update the JSON string below
json = "{}"
# create an instance of AddReaction200ResponseDataInner from a JSON string
add_reaction200_response_data_inner_instance = AddReaction200ResponseDataInner.from_json(json)
# print the JSON string representation of the object
print(AddReaction200ResponseDataInner.to_json())

# convert the object into a dict
add_reaction200_response_data_inner_dict = add_reaction200_response_data_inner_instance.to_dict()
# create an instance of AddReaction200ResponseDataInner from a dict
add_reaction200_response_data_inner_from_dict = AddReaction200ResponseDataInner.from_dict(add_reaction200_response_data_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


