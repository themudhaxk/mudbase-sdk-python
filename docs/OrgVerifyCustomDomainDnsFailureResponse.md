# OrgVerifyCustomDomainDnsFailureResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**success** | **bool** |  | 
**code** | **str** |  | 
**error** | **str** |  | 
**challenge_host** | **str** |  | 
**expected_txt** | **str** |  | 
**dns_txt_host** | **str** |  | 
**dns_txt_value** | **str** |  | 
**status** | **str** |  | 
**verification_token** | **str** |  | 

## Example

```python
from mudbase.models.org_verify_custom_domain_dns_failure_response import OrgVerifyCustomDomainDnsFailureResponse

# TODO update the JSON string below
json = "{}"
# create an instance of OrgVerifyCustomDomainDnsFailureResponse from a JSON string
org_verify_custom_domain_dns_failure_response_instance = OrgVerifyCustomDomainDnsFailureResponse.from_json(json)
# print the JSON string representation of the object
print(OrgVerifyCustomDomainDnsFailureResponse.to_json())

# convert the object into a dict
org_verify_custom_domain_dns_failure_response_dict = org_verify_custom_domain_dns_failure_response_instance.to_dict()
# create an instance of OrgVerifyCustomDomainDnsFailureResponse from a dict
org_verify_custom_domain_dns_failure_response_from_dict = OrgVerifyCustomDomainDnsFailureResponse.from_dict(org_verify_custom_domain_dns_failure_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


