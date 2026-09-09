# RemoveParticipantRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**user_id** | **str** |  | 

## Example

```python
from mudbase.models.remove_participant_request import RemoveParticipantRequest

# TODO update the JSON string below
json = "{}"
# create an instance of RemoveParticipantRequest from a JSON string
remove_participant_request_instance = RemoveParticipantRequest.from_json(json)
# print the JSON string representation of the object
print(RemoveParticipantRequest.to_json())

# convert the object into a dict
remove_participant_request_dict = remove_participant_request_instance.to_dict()
# create an instance of RemoveParticipantRequest from a dict
remove_participant_request_from_dict = RemoveParticipantRequest.from_dict(remove_participant_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


