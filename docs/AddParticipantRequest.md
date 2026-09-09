# AddParticipantRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**user_id** | **str** |  | 
**role** | **str** |  | [optional] 

## Example

```python
from mudbase.models.add_participant_request import AddParticipantRequest

# TODO update the JSON string below
json = "{}"
# create an instance of AddParticipantRequest from a JSON string
add_participant_request_instance = AddParticipantRequest.from_json(json)
# print the JSON string representation of the object
print(AddParticipantRequest.to_json())

# convert the object into a dict
add_participant_request_dict = add_participant_request_instance.to_dict()
# create an instance of AddParticipantRequest from a dict
add_participant_request_from_dict = AddParticipantRequest.from_dict(add_participant_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


