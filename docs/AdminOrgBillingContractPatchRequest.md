# AdminOrgBillingContractPatchRequest

At least one contract field required (excluding reason alone).

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**contract_amount_cents** | **int** |  | [optional] 
**contract_currency** | **str** |  | [optional] 
**contract_billing_interval** | **str** |  | [optional] 
**contract_effective_from** | **datetime** |  | [optional] 
**contract_notes** | **str** |  | [optional] 
**reason** | **str** |  | [optional] 

## Example

```python
from mudbase.models.admin_org_billing_contract_patch_request import AdminOrgBillingContractPatchRequest

# TODO update the JSON string below
json = "{}"
# create an instance of AdminOrgBillingContractPatchRequest from a JSON string
admin_org_billing_contract_patch_request_instance = AdminOrgBillingContractPatchRequest.from_json(json)
# print the JSON string representation of the object
print(AdminOrgBillingContractPatchRequest.to_json())

# convert the object into a dict
admin_org_billing_contract_patch_request_dict = admin_org_billing_contract_patch_request_instance.to_dict()
# create an instance of AdminOrgBillingContractPatchRequest from a dict
admin_org_billing_contract_patch_request_from_dict = AdminOrgBillingContractPatchRequest.from_dict(admin_org_billing_contract_patch_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


