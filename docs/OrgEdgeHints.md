# OrgEdgeHints

Managed edge TLS custom-hostname hints returned after Mudbase verification (when the edge TLS integration is configured)

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**saas_integration_enabled** | **bool** |  | [optional] 
**skipped** | **bool** |  | [optional] 
**reason** | **str** |  | [optional] 
**custom_hostname_id** | **str** |  | [optional] 
**hostname_status** | **str** |  | [optional] 
**ssl_status** | **str** |  | [optional] 
**ownership_verification** | [**OrgEdgeHintsOwnershipVerification**](OrgEdgeHintsOwnershipVerification.md) |  | [optional] 
**ssl_validation_records** | [**List[OrgSslValidationRecord]**](OrgSslValidationRecord.md) |  | [optional] 
**last_error** | **str** |  | [optional] 
**instructions** | **str** |  | [optional] 

## Example

```python
from mudbase.models.org_edge_hints import OrgEdgeHints

# TODO update the JSON string below
json = "{}"
# create an instance of OrgEdgeHints from a JSON string
org_edge_hints_instance = OrgEdgeHints.from_json(json)
# print the JSON string representation of the object
print(OrgEdgeHints.to_json())

# convert the object into a dict
org_edge_hints_dict = org_edge_hints_instance.to_dict()
# create an instance of OrgEdgeHints from a dict
org_edge_hints_from_dict = OrgEdgeHints.from_dict(org_edge_hints_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


