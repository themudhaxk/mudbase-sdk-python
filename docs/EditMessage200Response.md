# EditMessage200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**success** | **bool** |  | [optional] 
**data** | [**EditMessage200ResponseData**](EditMessage200ResponseData.md) |  | [optional] 

## Example

```python
from mudbase.models.edit_message200_response import EditMessage200Response

# TODO update the JSON string below
json = "{}"
# create an instance of EditMessage200Response from a JSON string
edit_message200_response_instance = EditMessage200Response.from_json(json)
# print the JSON string representation of the object
print(EditMessage200Response.to_json())

# convert the object into a dict
edit_message200_response_dict = edit_message200_response_instance.to_dict()
# create an instance of EditMessage200Response from a dict
edit_message200_response_from_dict = EditMessage200Response.from_dict(edit_message200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


