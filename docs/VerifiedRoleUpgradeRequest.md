# VerifiedRoleUpgradeRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**target_role** | **str** |  | 
**payment_intent_id** | **str** | Payment intent ID from payment provider | [optional] 
**verification_id** | **str** | KYC verification ID (if required) | [optional] 

## Example

```python
from mudbase.models.verified_role_upgrade_request import VerifiedRoleUpgradeRequest

# TODO update the JSON string below
json = "{}"
# create an instance of VerifiedRoleUpgradeRequest from a JSON string
verified_role_upgrade_request_instance = VerifiedRoleUpgradeRequest.from_json(json)
# print the JSON string representation of the object
print(VerifiedRoleUpgradeRequest.to_json())

# convert the object into a dict
verified_role_upgrade_request_dict = verified_role_upgrade_request_instance.to_dict()
# create an instance of VerifiedRoleUpgradeRequest from a dict
verified_role_upgrade_request_from_dict = VerifiedRoleUpgradeRequest.from_dict(verified_role_upgrade_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


