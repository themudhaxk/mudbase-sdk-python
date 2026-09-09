# AddParticipant200ResponseData


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**participants** | [**List[AddParticipant200ResponseDataParticipantsInner]**](AddParticipant200ResponseDataParticipantsInner.md) |  | [optional] 

## Example

```python
from mudbase.models.add_participant200_response_data import AddParticipant200ResponseData

# TODO update the JSON string below
json = "{}"
# create an instance of AddParticipant200ResponseData from a JSON string
add_participant200_response_data_instance = AddParticipant200ResponseData.from_json(json)
# print the JSON string representation of the object
print(AddParticipant200ResponseData.to_json())

# convert the object into a dict
add_participant200_response_data_dict = add_participant200_response_data_instance.to_dict()
# create an instance of AddParticipant200ResponseData from a dict
add_participant200_response_data_from_dict = AddParticipant200ResponseData.from_dict(add_participant200_response_data_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


