# OrgDomainEntryOrgConsole

Org API compact domain row: use **`dnsRecords`** for the Mudbase ownership TXT (purpose `mudbase_ownership`) and routing CNAME. Omits `hostnameNormalized`, `verificationToken`, `dnsTxtHost`, and `dnsTxtValue`. Omits `edge` when edge SSL is not configured. Optional keys with no value are omitted from JSON responses.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** |  | [optional] 
**hostname** | **str** |  | [optional] 
**status** | **str** |  | [optional] 
**is_primary** | **bool** |  | [optional] 
**source** | **str** |  | [optional] 
**created_at** | **datetime** |  | [optional] 
**verified_at** | **datetime** |  | [optional] 
**last_verified_at** | **datetime** |  | [optional] 
**cname_submitted_at** | **datetime** |  | [optional] 
**cname_approved_at** | **datetime** |  | [optional] 
**custom_domain_verification_step** | **int** |  | [optional] 
**routing_cname_target** | **str** |  | [optional] 
**dns_records** | [**List[OrgDnsRecord]**](OrgDnsRecord.md) |  | [optional] 
**platform_activation_pending** | **bool** |  | [optional] 
**custom_domain_live_for_api_traffic** | **bool** |  | [optional] 
**edge** | [**OrgEdgeHints**](OrgEdgeHints.md) |  | [optional] 
**fly_certificate_status** | **str** |  | [optional] 
**platform_dns_verification** | [**OrgPlatformDnsVerificationCustomer**](OrgPlatformDnsVerificationCustomer.md) |  | [optional] 
**platform_dns_verification_submitted_at** | **datetime** |  | [optional] 

## Example

```python
from mudbase.models.org_domain_entry_org_console import OrgDomainEntryOrgConsole

# TODO update the JSON string below
json = "{}"
# create an instance of OrgDomainEntryOrgConsole from a JSON string
org_domain_entry_org_console_instance = OrgDomainEntryOrgConsole.from_json(json)
# print the JSON string representation of the object
print(OrgDomainEntryOrgConsole.to_json())

# convert the object into a dict
org_domain_entry_org_console_dict = org_domain_entry_org_console_instance.to_dict()
# create an instance of OrgDomainEntryOrgConsole from a dict
org_domain_entry_org_console_from_dict = OrgDomainEntryOrgConsole.from_dict(org_domain_entry_org_console_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


