# OrgSslValidationRecord


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**txt_name** | **str** |  | [optional] 
**txt_value** | **str** |  | [optional] 
**http_url** | **str** |  | [optional] 
**http_body** | **str** |  | [optional] 
**cname** | **str** |  | [optional] 
**cname_target** | **str** |  | [optional] 

## Example

```python
from mudbase.models.org_ssl_validation_record import OrgSslValidationRecord

# TODO update the JSON string below
json = "{}"
# create an instance of OrgSslValidationRecord from a JSON string
org_ssl_validation_record_instance = OrgSslValidationRecord.from_json(json)
# print the JSON string representation of the object
print(OrgSslValidationRecord.to_json())

# convert the object into a dict
org_ssl_validation_record_dict = org_ssl_validation_record_instance.to_dict()
# create an instance of OrgSslValidationRecord from a dict
org_ssl_validation_record_from_dict = OrgSslValidationRecord.from_dict(org_ssl_validation_record_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


