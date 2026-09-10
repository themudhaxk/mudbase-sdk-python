# GetComplianceSummary200ResponseComplianceSecurity


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**password_policy** | **str** |  | [optional] 
**virus_scanning** | **bool** |  | [optional] 
**encryption_at_rest** | **bool** |  | [optional] 

## Example

```python
from mudbase.models.get_compliance_summary200_response_compliance_security import GetComplianceSummary200ResponseComplianceSecurity

# TODO update the JSON string below
json = "{}"
# create an instance of GetComplianceSummary200ResponseComplianceSecurity from a JSON string
get_compliance_summary200_response_compliance_security_instance = GetComplianceSummary200ResponseComplianceSecurity.from_json(json)
# print the JSON string representation of the object
print(GetComplianceSummary200ResponseComplianceSecurity.to_json())

# convert the object into a dict
get_compliance_summary200_response_compliance_security_dict = get_compliance_summary200_response_compliance_security_instance.to_dict()
# create an instance of GetComplianceSummary200ResponseComplianceSecurity from a dict
get_compliance_summary200_response_compliance_security_from_dict = GetComplianceSummary200ResponseComplianceSecurity.from_dict(get_compliance_summary200_response_compliance_security_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


