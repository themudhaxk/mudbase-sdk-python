# AdminPlatformDnsVerificationPatchRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**record_type** | **str** |  | [optional] 
**record_name** | **str** |  | 
**record_value** | **str** |  | 
**ttl_seconds** | **int** |  | [optional] 
**staff_note** | **str** |  | [optional] 
**reset_customer_platform_dns_submission** | **bool** |  | [optional] 
**notify_org** | **bool** | When not false (default), email org billing contact with step-3 DNS instructions after save. | [optional] 

## Example

```python
from mudbase.models.admin_platform_dns_verification_patch_request import AdminPlatformDnsVerificationPatchRequest

# TODO update the JSON string below
json = "{}"
# create an instance of AdminPlatformDnsVerificationPatchRequest from a JSON string
admin_platform_dns_verification_patch_request_instance = AdminPlatformDnsVerificationPatchRequest.from_json(json)
# print the JSON string representation of the object
print(AdminPlatformDnsVerificationPatchRequest.to_json())

# convert the object into a dict
admin_platform_dns_verification_patch_request_dict = admin_platform_dns_verification_patch_request_instance.to_dict()
# create an instance of AdminPlatformDnsVerificationPatchRequest from a dict
admin_platform_dns_verification_patch_request_from_dict = AdminPlatformDnsVerificationPatchRequest.from_dict(admin_platform_dns_verification_patch_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


