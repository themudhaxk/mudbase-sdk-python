# AdminOrgLimitsPatchRequestBugAnalysis


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**scans_per_month** | **int** |  | [optional] 
**max_upload_bytes** | **int** |  | [optional] 
**max_runtime_minutes** | **int** |  | [optional] 
**queue_type** | **str** |  | [optional] 
**log_retention_days** | **int** |  | [optional] 

## Example

```python
from mudbase.models.admin_org_limits_patch_request_bug_analysis import AdminOrgLimitsPatchRequestBugAnalysis

# TODO update the JSON string below
json = "{}"
# create an instance of AdminOrgLimitsPatchRequestBugAnalysis from a JSON string
admin_org_limits_patch_request_bug_analysis_instance = AdminOrgLimitsPatchRequestBugAnalysis.from_json(json)
# print the JSON string representation of the object
print(AdminOrgLimitsPatchRequestBugAnalysis.to_json())

# convert the object into a dict
admin_org_limits_patch_request_bug_analysis_dict = admin_org_limits_patch_request_bug_analysis_instance.to_dict()
# create an instance of AdminOrgLimitsPatchRequestBugAnalysis from a dict
admin_org_limits_patch_request_bug_analysis_from_dict = AdminOrgLimitsPatchRequestBugAnalysis.from_dict(admin_org_limits_patch_request_bug_analysis_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


