# AdminOrgLimitsPatchRequest

Partial org limit overrides for platform admins. At least one property required. Keys match `PLANS[*].limits` in the backend; integers are non-negative or null for unlimited. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**projects** | **int** |  | [optional] 
**storage** | **int** |  | [optional] 
**bandwidth** | **int** |  | [optional] 
**api_calls** | **int** |  | [optional] 
**buckets** | **int** |  | [optional] 
**collections** | **int** |  | [optional] 
**realtime_connections** | **int** |  | [optional] 
**realtime_messages** | **int** |  | [optional] 
**chat_messages_per_month** | **int** |  | [optional] 
**api_keys_per_project** | **int** |  | [optional] 
**webhooks_per_project** | **int** |  | [optional] 
**functions_per_project** | **int** |  | [optional] 
**function_invocations_per_month** | **int** |  | [optional] 
**messaging_messages_per_month** | **int** |  | [optional] 
**sms_per_month** | **int** |  | [optional] 
**chat_channels_per_project** | **int** |  | [optional] 
**backups_per_project** | **int** |  | [optional] 
**restores_per_month** | **int** |  | [optional] 
**integrations_per_project** | **int** |  | [optional] 
**roles_per_org** | **int** |  | [optional] 
**alerts_per_project** | **int** |  | [optional] 
**blockchain_chains** | **int** |  | [optional] 
**team_users** | **int** |  | [optional] 
**bug_analysis** | [**AdminOrgLimitsPatchRequestBugAnalysis**](AdminOrgLimitsPatchRequestBugAnalysis.md) |  | [optional] 

## Example

```python
from mudbase.models.admin_org_limits_patch_request import AdminOrgLimitsPatchRequest

# TODO update the JSON string below
json = "{}"
# create an instance of AdminOrgLimitsPatchRequest from a JSON string
admin_org_limits_patch_request_instance = AdminOrgLimitsPatchRequest.from_json(json)
# print the JSON string representation of the object
print(AdminOrgLimitsPatchRequest.to_json())

# convert the object into a dict
admin_org_limits_patch_request_dict = admin_org_limits_patch_request_instance.to_dict()
# create an instance of AdminOrgLimitsPatchRequest from a dict
admin_org_limits_patch_request_from_dict = AdminOrgLimitsPatchRequest.from_dict(admin_org_limits_patch_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


