# InviteSubOrganizationMember200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**message** | **str** |  | [optional] 
**email** | **str** |  | [optional] 
**role** | **str** |  | [optional] 

## Example

```python
from mudbase.models.invite_sub_organization_member200_response import InviteSubOrganizationMember200Response

# TODO update the JSON string below
json = "{}"
# create an instance of InviteSubOrganizationMember200Response from a JSON string
invite_sub_organization_member200_response_instance = InviteSubOrganizationMember200Response.from_json(json)
# print the JSON string representation of the object
print(InviteSubOrganizationMember200Response.to_json())

# convert the object into a dict
invite_sub_organization_member200_response_dict = invite_sub_organization_member200_response_instance.to_dict()
# create an instance of InviteSubOrganizationMember200Response from a dict
invite_sub_organization_member200_response_from_dict = InviteSubOrganizationMember200Response.from_dict(invite_sub_organization_member200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


