# VerifyProjectEmailSmtpDomainRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**domain** | **str** |  | [optional] 
**from_email** | **str** |  | [optional] 
**persist** | **bool** | If true and checks pass, persist domainVerifiedAt on the project | [optional] 

## Example

```python
from mudbase.models.verify_project_email_smtp_domain_request import VerifyProjectEmailSmtpDomainRequest

# TODO update the JSON string below
json = "{}"
# create an instance of VerifyProjectEmailSmtpDomainRequest from a JSON string
verify_project_email_smtp_domain_request_instance = VerifyProjectEmailSmtpDomainRequest.from_json(json)
# print the JSON string representation of the object
print(VerifyProjectEmailSmtpDomainRequest.to_json())

# convert the object into a dict
verify_project_email_smtp_domain_request_dict = verify_project_email_smtp_domain_request_instance.to_dict()
# create an instance of VerifyProjectEmailSmtpDomainRequest from a dict
verify_project_email_smtp_domain_request_from_dict = VerifyProjectEmailSmtpDomainRequest.from_dict(verify_project_email_smtp_domain_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


