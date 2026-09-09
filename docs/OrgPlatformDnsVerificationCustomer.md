# OrgPlatformDnsVerificationCustomer

Additional DNS record from platform staff (manual path), or the first certificate-provisioning TXT shim when automated provisioning is enabled. Prefer `dnsRecords` for full instructions. `staffNote` may appear in admin org detail only.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**record_type** | **str** |  | [optional] 
**record_name** | **str** |  | [optional] 
**record_value** | **str** |  | [optional] 
**ttl_seconds** | **int** |  | [optional] 
**staff_note** | **str** |  | [optional] 
**updated_at** | **datetime** |  | [optional] 

## Example

```python
from mudbase.models.org_platform_dns_verification_customer import OrgPlatformDnsVerificationCustomer

# TODO update the JSON string below
json = "{}"
# create an instance of OrgPlatformDnsVerificationCustomer from a JSON string
org_platform_dns_verification_customer_instance = OrgPlatformDnsVerificationCustomer.from_json(json)
# print the JSON string representation of the object
print(OrgPlatformDnsVerificationCustomer.to_json())

# convert the object into a dict
org_platform_dns_verification_customer_dict = org_platform_dns_verification_customer_instance.to_dict()
# create an instance of OrgPlatformDnsVerificationCustomer from a dict
org_platform_dns_verification_customer_from_dict = OrgPlatformDnsVerificationCustomer.from_dict(org_platform_dns_verification_customer_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


