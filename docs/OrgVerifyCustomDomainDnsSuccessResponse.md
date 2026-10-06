# OrgVerifyCustomDomainDnsSuccessResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**success** | **bool** |  | 
**hostname** | **str** |  | 
**status** | **str** | Domain row status after check (typically cname_pending_staff after first TXT success from pending/failed; legacy dns_verified possible) | 
**verification_token** | **str** |  | 
**challenge_host** | **str** | Same as dnsTxtHost (_mudbase-verify.&lt;hostname&gt;) | 
**expected_txt** | **str** | Same as dnsTxtValue | 
**dns_txt_host** | **str** |  | 
**dns_txt_value** | **str** |  | 
**edge** | [**OrgEdgeHints**](OrgEdgeHints.md) |  | [optional] 
**dns_records** | [**List[OrgDnsRecord]**](OrgDnsRecord.md) | Same shape as &#x60;OrgDomainEntryWithDns.dnsRecords&#x60; when certificate provisioning ran after this successful verify; omit or empty when provisioning is disabled or not yet run. | [optional] 
**fly_certificate_status** | **str** | Managed certificate status after verify when provisioning is active; null otherwise | [optional] 
**fly_acme_enabled** | **bool** | True when automated managed-certificate provisioning is configured for this deployment. | [optional] 
**fly_acme_disabled_reason** | **str** | When &#x60;flyAcmeEnabled&#x60; is false, why automated provisioning did not run (ops misconfiguration hint). | [optional] 
**fly_provision_error** | **str** | When provisioning is enabled but certificate issuance failed, the provider error message for support; null on success. | [optional] 
**fly_legacy_staff_pipeline** | **bool** | When true, the legacy staff pipeline is on: status may stay &#x60;cname_pending_staff&#x60; and staff approve-cname is required even if certificate provisioning succeeds. | [optional] 

## Example

```python
from mudbase.models.org_verify_custom_domain_dns_success_response import OrgVerifyCustomDomainDnsSuccessResponse

# TODO update the JSON string below
json = "{}"
# create an instance of OrgVerifyCustomDomainDnsSuccessResponse from a JSON string
org_verify_custom_domain_dns_success_response_instance = OrgVerifyCustomDomainDnsSuccessResponse.from_json(json)
# print the JSON string representation of the object
print(OrgVerifyCustomDomainDnsSuccessResponse.to_json())

# convert the object into a dict
org_verify_custom_domain_dns_success_response_dict = org_verify_custom_domain_dns_success_response_instance.to_dict()
# create an instance of OrgVerifyCustomDomainDnsSuccessResponse from a dict
org_verify_custom_domain_dns_success_response_from_dict = OrgVerifyCustomDomainDnsSuccessResponse.from_dict(org_verify_custom_domain_dns_success_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


