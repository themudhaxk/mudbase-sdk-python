# ProvisionEnterpriseRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**org_id** | **str** |  | 
**provision_request_id** | **str** |  | 
**api_base_url** | **str** |  | 
**db_ref** | **str** |  | 
**server_id** | **str** |  | 
**region** | **str** |  | [optional] 
**version** | **str** |  | [optional] 
**force_override** | **bool** |  | [optional] 

## Example

```python
from mudbase.models.provision_enterprise_request import ProvisionEnterpriseRequest

# TODO update the JSON string below
json = "{}"
# create an instance of ProvisionEnterpriseRequest from a JSON string
provision_enterprise_request_instance = ProvisionEnterpriseRequest.from_json(json)
# print the JSON string representation of the object
print(ProvisionEnterpriseRequest.to_json())

# convert the object into a dict
provision_enterprise_request_dict = provision_enterprise_request_instance.to_dict()
# create an instance of ProvisionEnterpriseRequest from a dict
provision_enterprise_request_from_dict = ProvisionEnterpriseRequest.from_dict(provision_enterprise_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


