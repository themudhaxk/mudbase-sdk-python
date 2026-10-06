# OrgDnsInstructionsResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**success** | **bool** |  | 
**domain** | [**OrgDomainEntryOrgConsole**](OrgDomainEntryOrgConsole.md) |  | 
**dns_verification_instructions** | **str** | Plain-language reminder to add the ownership TXT from the domain’s DNS checklist, then use Verify DNS in the organization’s domain settings. | [optional] 

## Example

```python
from mudbase.models.org_dns_instructions_response import OrgDnsInstructionsResponse

# TODO update the JSON string below
json = "{}"
# create an instance of OrgDnsInstructionsResponse from a JSON string
org_dns_instructions_response_instance = OrgDnsInstructionsResponse.from_json(json)
# print the JSON string representation of the object
print(OrgDnsInstructionsResponse.to_json())

# convert the object into a dict
org_dns_instructions_response_dict = org_dns_instructions_response_instance.to_dict()
# create an instance of OrgDnsInstructionsResponse from a dict
org_dns_instructions_response_from_dict = OrgDnsInstructionsResponse.from_dict(org_dns_instructions_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


