# AdminProvisionEnterpriseBody


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**provision_request_id** | **str** |  | 
**api_base_url** | **str** |  | 
**db_ref** | **str** |  | 
**server_id** | **str** |  | 
**region** | **str** |  | [optional] 
**version** | **str** |  | [optional] 
**force_override** | **bool** |  | [optional] 

## Example

```python
from mudbase.models.admin_provision_enterprise_body import AdminProvisionEnterpriseBody

# TODO update the JSON string below
json = "{}"
# create an instance of AdminProvisionEnterpriseBody from a JSON string
admin_provision_enterprise_body_instance = AdminProvisionEnterpriseBody.from_json(json)
# print the JSON string representation of the object
print(AdminProvisionEnterpriseBody.to_json())

# convert the object into a dict
admin_provision_enterprise_body_dict = admin_provision_enterprise_body_instance.to_dict()
# create an instance of AdminProvisionEnterpriseBody from a dict
admin_provision_enterprise_body_from_dict = AdminProvisionEnterpriseBody.from_dict(admin_provision_enterprise_body_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


