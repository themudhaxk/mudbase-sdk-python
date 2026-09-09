# AddParticipant200ResponseDataParticipantsInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**user_id** | **str** |  | [optional] 
**role** | **str** |  | [optional] 
**added_at** | **datetime** |  | [optional] 

## Example

```python
from mudbase.models.add_participant200_response_data_participants_inner import AddParticipant200ResponseDataParticipantsInner

# TODO update the JSON string below
json = "{}"
# create an instance of AddParticipant200ResponseDataParticipantsInner from a JSON string
add_participant200_response_data_participants_inner_instance = AddParticipant200ResponseDataParticipantsInner.from_json(json)
# print the JSON string representation of the object
print(AddParticipant200ResponseDataParticipantsInner.to_json())

# convert the object into a dict
add_participant200_response_data_participants_inner_dict = add_participant200_response_data_participants_inner_instance.to_dict()
# create an instance of AddParticipant200ResponseDataParticipantsInner from a dict
add_participant200_response_data_participants_inner_from_dict = AddParticipant200ResponseDataParticipantsInner.from_dict(add_participant200_response_data_participants_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


