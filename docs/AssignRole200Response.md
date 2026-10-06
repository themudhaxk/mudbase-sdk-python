# AssignRole200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**message** | **str** |  | [optional] 
**user** | **object** |  | [optional] 

## Example

```python
from mudbase.models.assign_role200_response import AssignRole200Response

# TODO update the JSON string below
json = "{}"
# create an instance of AssignRole200Response from a JSON string
assign_role200_response_instance = AssignRole200Response.from_json(json)
# print the JSON string representation of the object
print(AssignRole200Response.to_json())

# convert the object into a dict
assign_role200_response_dict = assign_role200_response_instance.to_dict()
# create an instance of AssignRole200Response from a dict
assign_role200_response_from_dict = AssignRole200Response.from_dict(assign_role200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


