# GetComplianceSummary200ResponseComplianceGdpr


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**data_export_enabled** | **bool** |  | [optional] 
**data_erasure_enabled** | **bool** |  | [optional] 
**consent_management** | **bool** |  | [optional] 

## Example

```python
from mudbase.models.get_compliance_summary200_response_compliance_gdpr import GetComplianceSummary200ResponseComplianceGdpr

# TODO update the JSON string below
json = "{}"
# create an instance of GetComplianceSummary200ResponseComplianceGdpr from a JSON string
get_compliance_summary200_response_compliance_gdpr_instance = GetComplianceSummary200ResponseComplianceGdpr.from_json(json)
# print the JSON string representation of the object
print(GetComplianceSummary200ResponseComplianceGdpr.to_json())

# convert the object into a dict
get_compliance_summary200_response_compliance_gdpr_dict = get_compliance_summary200_response_compliance_gdpr_instance.to_dict()
# create an instance of GetComplianceSummary200ResponseComplianceGdpr from a dict
get_compliance_summary200_response_compliance_gdpr_from_dict = GetComplianceSummary200ResponseComplianceGdpr.from_dict(get_compliance_summary200_response_compliance_gdpr_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


