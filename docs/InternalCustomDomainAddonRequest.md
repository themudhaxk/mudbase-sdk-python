# InternalCustomDomainAddonRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**org_id** | **str** |  | 
**enabled** | **bool** |  | 

## Example

```python
from mudbase.models.internal_custom_domain_addon_request import InternalCustomDomainAddonRequest

# TODO update the JSON string below
json = "{}"
# create an instance of InternalCustomDomainAddonRequest from a JSON string
internal_custom_domain_addon_request_instance = InternalCustomDomainAddonRequest.from_json(json)
# print the JSON string representation of the object
print(InternalCustomDomainAddonRequest.to_json())

# convert the object into a dict
internal_custom_domain_addon_request_dict = internal_custom_domain_addon_request_instance.to_dict()
# create an instance of InternalCustomDomainAddonRequest from a dict
internal_custom_domain_addon_request_from_dict = InternalCustomDomainAddonRequest.from_dict(internal_custom_domain_addon_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


