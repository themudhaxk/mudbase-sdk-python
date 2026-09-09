# PatchOrgDomainRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**status** | **str** | Org self-serve reset only; go-live is via admin activate. | [optional] 
**regenerate_token** | **bool** |  | [optional] 

## Example

```python
from mudbase.models.patch_org_domain_request import PatchOrgDomainRequest

# TODO update the JSON string below
json = "{}"
# create an instance of PatchOrgDomainRequest from a JSON string
patch_org_domain_request_instance = PatchOrgDomainRequest.from_json(json)
# print the JSON string representation of the object
print(PatchOrgDomainRequest.to_json())

# convert the object into a dict
patch_org_domain_request_dict = patch_org_domain_request_instance.to_dict()
# create an instance of PatchOrgDomainRequest from a dict
patch_org_domain_request_from_dict = PatchOrgDomainRequest.from_dict(patch_org_domain_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


