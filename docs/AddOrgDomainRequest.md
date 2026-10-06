# AddOrgDomainRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**hostname** | **str** |  | 
**set_primary** | **bool** |  | [optional] 

## Example

```python
from mudbase.models.add_org_domain_request import AddOrgDomainRequest

# TODO update the JSON string below
json = "{}"
# create an instance of AddOrgDomainRequest from a JSON string
add_org_domain_request_instance = AddOrgDomainRequest.from_json(json)
# print the JSON string representation of the object
print(AddOrgDomainRequest.to_json())

# convert the object into a dict
add_org_domain_request_dict = add_org_domain_request_instance.to_dict()
# create an instance of AddOrgDomainRequest from a dict
add_org_domain_request_from_dict = AddOrgDomainRequest.from_dict(add_org_domain_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


