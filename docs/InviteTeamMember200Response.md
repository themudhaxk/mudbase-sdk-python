# InviteTeamMember200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**message** | **str** |  | [optional] 
**email** | **str** |  | [optional] 
**role** | **str** |  | [optional] 

## Example

```python
from mudbase.models.invite_team_member200_response import InviteTeamMember200Response

# TODO update the JSON string below
json = "{}"
# create an instance of InviteTeamMember200Response from a JSON string
invite_team_member200_response_instance = InviteTeamMember200Response.from_json(json)
# print the JSON string representation of the object
print(InviteTeamMember200Response.to_json())

# convert the object into a dict
invite_team_member200_response_dict = invite_team_member200_response_instance.to_dict()
# create an instance of InviteTeamMember200Response from a dict
invite_team_member200_response_from_dict = InviteTeamMember200Response.from_dict(invite_team_member200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


