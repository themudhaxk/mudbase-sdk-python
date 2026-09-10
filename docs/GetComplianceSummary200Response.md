# GetComplianceSummary200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**compliance** | [**GetComplianceSummary200ResponseCompliance**](GetComplianceSummary200ResponseCompliance.md) |  | [optional] 

## Example

```python
from mudbase.models.get_compliance_summary200_response import GetComplianceSummary200Response

# TODO update the JSON string below
json = "{}"
# create an instance of GetComplianceSummary200Response from a JSON string
get_compliance_summary200_response_instance = GetComplianceSummary200Response.from_json(json)
# print the JSON string representation of the object
print(GetComplianceSummary200Response.to_json())

# convert the object into a dict
get_compliance_summary200_response_dict = get_compliance_summary200_response_instance.to_dict()
# create an instance of GetComplianceSummary200Response from a dict
get_compliance_summary200_response_from_dict = GetComplianceSummary200Response.from_dict(get_compliance_summary200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


