# VerifiedRoleUpgrade200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**message** | **str** |  | [optional] 
**role** | **str** |  | [optional] 
**previous_role** | **str** |  | [optional] 
**upgrade_log** | **str** |  | [optional] 

## Example

```python
from mudbase.models.verified_role_upgrade200_response import VerifiedRoleUpgrade200Response

# TODO update the JSON string below
json = "{}"
# create an instance of VerifiedRoleUpgrade200Response from a JSON string
verified_role_upgrade200_response_instance = VerifiedRoleUpgrade200Response.from_json(json)
# print the JSON string representation of the object
print(VerifiedRoleUpgrade200Response.to_json())

# convert the object into a dict
verified_role_upgrade200_response_dict = verified_role_upgrade200_response_instance.to_dict()
# create an instance of VerifiedRoleUpgrade200Response from a dict
verified_role_upgrade200_response_from_dict = VerifiedRoleUpgrade200Response.from_dict(verified_role_upgrade200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


