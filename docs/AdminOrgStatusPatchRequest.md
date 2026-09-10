# AdminOrgStatusPatchRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**is_active** | **bool** |  | 
**platform_suspended_reason** | **str** |  | [optional] 
**platform_admin_note** | **str** |  | [optional] 
**reason** | **str** |  | [optional] 

## Example

```python
from mudbase.models.admin_org_status_patch_request import AdminOrgStatusPatchRequest

# TODO update the JSON string below
json = "{}"
# create an instance of AdminOrgStatusPatchRequest from a JSON string
admin_org_status_patch_request_instance = AdminOrgStatusPatchRequest.from_json(json)
# print the JSON string representation of the object
print(AdminOrgStatusPatchRequest.to_json())

# convert the object into a dict
admin_org_status_patch_request_dict = admin_org_status_patch_request_instance.to_dict()
# create an instance of AdminOrgStatusPatchRequest from a dict
admin_org_status_patch_request_from_dict = AdminOrgStatusPatchRequest.from_dict(admin_org_status_patch_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


