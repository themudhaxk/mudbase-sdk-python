# RemoveReaction200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**success** | **bool** |  | [optional] 
**data** | [**List[RemoveReaction200ResponseDataInner]**](RemoveReaction200ResponseDataInner.md) |  | [optional] 

## Example

```python
from mudbase.models.remove_reaction200_response import RemoveReaction200Response

# TODO update the JSON string below
json = "{}"
# create an instance of RemoveReaction200Response from a JSON string
remove_reaction200_response_instance = RemoveReaction200Response.from_json(json)
# print the JSON string representation of the object
print(RemoveReaction200Response.to_json())

# convert the object into a dict
remove_reaction200_response_dict = remove_reaction200_response_instance.to_dict()
# create an instance of RemoveReaction200Response from a dict
remove_reaction200_response_from_dict = RemoveReaction200Response.from_dict(remove_reaction200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


