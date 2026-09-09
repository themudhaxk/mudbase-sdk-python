# InternalDomainDnsRecheckBatchRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**max_orgs** | **int** |  | [optional] 
**recheck_older_than_hours** | **int** |  | [optional] 

## Example

```python
from mudbase.models.internal_domain_dns_recheck_batch_request import InternalDomainDnsRecheckBatchRequest

# TODO update the JSON string below
json = "{}"
# create an instance of InternalDomainDnsRecheckBatchRequest from a JSON string
internal_domain_dns_recheck_batch_request_instance = InternalDomainDnsRecheckBatchRequest.from_json(json)
# print the JSON string representation of the object
print(InternalDomainDnsRecheckBatchRequest.to_json())

# convert the object into a dict
internal_domain_dns_recheck_batch_request_dict = internal_domain_dns_recheck_batch_request_instance.to_dict()
# create an instance of InternalDomainDnsRecheckBatchRequest from a dict
internal_domain_dns_recheck_batch_request_from_dict = InternalDomainDnsRecheckBatchRequest.from_dict(internal_domain_dns_recheck_batch_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


