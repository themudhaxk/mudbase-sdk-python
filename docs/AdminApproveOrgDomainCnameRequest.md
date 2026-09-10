# AdminApproveOrgDomainCnameRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**verify_dns** | **bool** | When true, public DNS CNAME chain for hostname must match Fly &#x60;dns_requirements.cname&#x60; when stored, else &#x60;CUSTOM_DOMAIN_API_CNAME_TARGET&#x60;. | [optional] 

## Example

```python
from mudbase.models.admin_approve_org_domain_cname_request import AdminApproveOrgDomainCnameRequest

# TODO update the JSON string below
json = "{}"
# create an instance of AdminApproveOrgDomainCnameRequest from a JSON string
admin_approve_org_domain_cname_request_instance = AdminApproveOrgDomainCnameRequest.from_json(json)
# print the JSON string representation of the object
print(AdminApproveOrgDomainCnameRequest.to_json())

# convert the object into a dict
admin_approve_org_domain_cname_request_dict = admin_approve_org_domain_cname_request_instance.to_dict()
# create an instance of AdminApproveOrgDomainCnameRequest from a dict
admin_approve_org_domain_cname_request_from_dict = AdminApproveOrgDomainCnameRequest.from_dict(admin_approve_org_domain_cname_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


