# OrgDomainsListResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**domains** | [**List[OrgDomainEntryOrgConsole]**](OrgDomainEntryOrgConsole.md) |  | [optional] 
**dns_verification_instructions** | **str** | Plain-language reminder to add the ownership TXT from each domain’s DNS checklist, then use Verify DNS in the organization’s domain settings. | [optional] 
**primary_hostname** | **str** |  | [optional] 
**api_base_url** | **str** |  | [optional] 
**max_domains** | **int** |  | [optional] 
**custom_domain_allowed** | **bool** |  | [optional] 

## Example

```python
from mudbase.models.org_domains_list_response import OrgDomainsListResponse

# TODO update the JSON string below
json = "{}"
# create an instance of OrgDomainsListResponse from a JSON string
org_domains_list_response_instance = OrgDomainsListResponse.from_json(json)
# print the JSON string representation of the object
print(OrgDomainsListResponse.to_json())

# convert the object into a dict
org_domains_list_response_dict = org_domains_list_response_instance.to_dict()
# create an instance of OrgDomainsListResponse from a dict
org_domains_list_response_from_dict = OrgDomainsListResponse.from_dict(org_domains_list_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


