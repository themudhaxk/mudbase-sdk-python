# AddParticipant200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**success** | **bool** |  | [optional] 
**data** | [**AddParticipant200ResponseData**](AddParticipant200ResponseData.md) |  | [optional] 

## Example

```python
from mudbase.models.add_participant200_response import AddParticipant200Response

# TODO update the JSON string below
json = "{}"
# create an instance of AddParticipant200Response from a JSON string
add_participant200_response_instance = AddParticipant200Response.from_json(json)
# print the JSON string representation of the object
print(AddParticipant200Response.to_json())

# convert the object into a dict
add_participant200_response_dict = add_participant200_response_instance.to_dict()
# create an instance of AddParticipant200Response from a dict
add_participant200_response_from_dict = AddParticipant200Response.from_dict(add_participant200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


