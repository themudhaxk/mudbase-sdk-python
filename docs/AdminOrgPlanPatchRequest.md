# AdminOrgPlanPatchRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**plan** | **str** |  | 
**reason** | **str** |  | [optional] 
**tx_plan** | **str** |  | [optional] 

## Example

```python
from mudbase.models.admin_org_plan_patch_request import AdminOrgPlanPatchRequest

# TODO update the JSON string below
json = "{}"
# create an instance of AdminOrgPlanPatchRequest from a JSON string
admin_org_plan_patch_request_instance = AdminOrgPlanPatchRequest.from_json(json)
# print the JSON string representation of the object
print(AdminOrgPlanPatchRequest.to_json())

# convert the object into a dict
admin_org_plan_patch_request_dict = admin_org_plan_patch_request_instance.to_dict()
# create an instance of AdminOrgPlanPatchRequest from a dict
admin_org_plan_patch_request_from_dict = AdminOrgPlanPatchRequest.from_dict(admin_org_plan_patch_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


