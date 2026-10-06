# AddReactionRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**emoji** | **str** |  | 

## Example

```python
from mudbase.models.add_reaction_request import AddReactionRequest

# TODO update the JSON string below
json = "{}"
# create an instance of AddReactionRequest from a JSON string
add_reaction_request_instance = AddReactionRequest.from_json(json)
# print the JSON string representation of the object
print(AddReactionRequest.to_json())

# convert the object into a dict
add_reaction_request_dict = add_reaction_request_instance.to_dict()
# create an instance of AddReactionRequest from a dict
add_reaction_request_from_dict = AddReactionRequest.from_dict(add_reaction_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


