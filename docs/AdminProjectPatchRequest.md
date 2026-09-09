# AdminProjectPatchRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** |  | [optional] 
**slug** | **str** |  | [optional] 
**is_archived** | **bool** |  | [optional] 

## Example

```python
from mudbase.models.admin_project_patch_request import AdminProjectPatchRequest

# TODO update the JSON string below
json = "{}"
# create an instance of AdminProjectPatchRequest from a JSON string
admin_project_patch_request_instance = AdminProjectPatchRequest.from_json(json)
# print the JSON string representation of the object
print(AdminProjectPatchRequest.to_json())

# convert the object into a dict
admin_project_patch_request_dict = admin_project_patch_request_instance.to_dict()
# create an instance of AdminProjectPatchRequest from a dict
admin_project_patch_request_from_dict = AdminProjectPatchRequest.from_dict(admin_project_patch_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


