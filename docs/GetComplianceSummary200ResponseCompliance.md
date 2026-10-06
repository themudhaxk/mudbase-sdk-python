# GetComplianceSummary200ResponseCompliance


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**gdpr** | [**GetComplianceSummary200ResponseComplianceGdpr**](GetComplianceSummary200ResponseComplianceGdpr.md) |  | [optional] 
**soc2** | [**GetComplianceSummary200ResponseComplianceSoc2**](GetComplianceSummary200ResponseComplianceSoc2.md) |  | [optional] 
**security** | [**GetComplianceSummary200ResponseComplianceSecurity**](GetComplianceSummary200ResponseComplianceSecurity.md) |  | [optional] 

## Example

```python
from mudbase.models.get_compliance_summary200_response_compliance import GetComplianceSummary200ResponseCompliance

# TODO update the JSON string below
json = "{}"
# create an instance of GetComplianceSummary200ResponseCompliance from a JSON string
get_compliance_summary200_response_compliance_instance = GetComplianceSummary200ResponseCompliance.from_json(json)
# print the JSON string representation of the object
print(GetComplianceSummary200ResponseCompliance.to_json())

# convert the object into a dict
get_compliance_summary200_response_compliance_dict = get_compliance_summary200_response_compliance_instance.to_dict()
# create an instance of GetComplianceSummary200ResponseCompliance from a dict
get_compliance_summary200_response_compliance_from_dict = GetComplianceSummary200ResponseCompliance.from_dict(get_compliance_summary200_response_compliance_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


