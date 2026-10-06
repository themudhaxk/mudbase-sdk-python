# VerifyEmailAuthRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**token** | **str** | Verification token from the email link | 
**project_id** | **str** | Optional; for project signup context (redirect hint) | [optional] 

## Example

```python
from mudbase.models.verify_email_auth_request import VerifyEmailAuthRequest

# TODO update the JSON string below
json = "{}"
# create an instance of VerifyEmailAuthRequest from a JSON string
verify_email_auth_request_instance = VerifyEmailAuthRequest.from_json(json)
# print the JSON string representation of the object
print(VerifyEmailAuthRequest.to_json())

# convert the object into a dict
verify_email_auth_request_dict = verify_email_auth_request_instance.to_dict()
# create an instance of VerifyEmailAuthRequest from a dict
verify_email_auth_request_from_dict = VerifyEmailAuthRequest.from_dict(verify_email_auth_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


