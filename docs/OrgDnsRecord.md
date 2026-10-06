# OrgDnsRecord


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**type** | **str** | DNS record type (TXT, CNAME, …) | 
**name** | **str** | Owner name / FQDN to create at the customer&#39;s DNS host | 
**value** | **str** | Record value or CNAME target | 
**purpose** | **str** | mudbase_ownership, routing, fly_ownership, acme_challenge, or fly (legacy bucket). | 

## Example

```python
from mudbase.models.org_dns_record import OrgDnsRecord

# TODO update the JSON string below
json = "{}"
# create an instance of OrgDnsRecord from a JSON string
org_dns_record_instance = OrgDnsRecord.from_json(json)
# print the JSON string representation of the object
print(OrgDnsRecord.to_json())

# convert the object into a dict
org_dns_record_dict = org_dns_record_instance.to_dict()
# create an instance of OrgDnsRecord from a dict
org_dns_record_from_dict = OrgDnsRecord.from_dict(org_dns_record_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


