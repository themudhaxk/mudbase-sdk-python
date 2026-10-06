# AddReaction200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**success** | **bool** |  | [optional] 
**data** | [**List[AddReaction200ResponseDataInner]**](AddReaction200ResponseDataInner.md) |  | [optional] 

## Example

```python
from mudbase.models.add_reaction200_response import AddReaction200Response

# TODO update the JSON string below
json = "{}"
# create an instance of AddReaction200Response from a JSON string
add_reaction200_response_instance = AddReaction200Response.from_json(json)
# print the JSON string representation of the object
print(AddReaction200Response.to_json())

# convert the object into a dict
add_reaction200_response_dict = add_reaction200_response_instance.to_dict()
# create an instance of AddReaction200Response from a dict
add_reaction200_response_from_dict = AddReaction200Response.from_dict(add_reaction200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


