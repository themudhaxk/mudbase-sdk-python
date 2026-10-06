# AdminMemberRolePatchRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**role** | **str** |  | 
**reason** | **str** |  | [optional] 

## Example

```python
from mudbase.models.admin_member_role_patch_request import AdminMemberRolePatchRequest

# TODO update the JSON string below
json = "{}"
# create an instance of AdminMemberRolePatchRequest from a JSON string
admin_member_role_patch_request_instance = AdminMemberRolePatchRequest.from_json(json)
# print the JSON string representation of the object
print(AdminMemberRolePatchRequest.to_json())

# convert the object into a dict
admin_member_role_patch_request_dict = admin_member_role_patch_request_instance.to_dict()
# create an instance of AdminMemberRolePatchRequest from a dict
admin_member_role_patch_request_from_dict = AdminMemberRolePatchRequest.from_dict(admin_member_role_patch_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


