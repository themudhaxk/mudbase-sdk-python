# ResendVerificationAuthRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**email** | **str** |  | 
**project_id** | **str** | Optional; for project-scoped signup (sends link with project context) | [optional] 

## Example

```python
from mudbase.models.resend_verification_auth_request import ResendVerificationAuthRequest

# TODO update the JSON string below
json = "{}"
# create an instance of ResendVerificationAuthRequest from a JSON string
resend_verification_auth_request_instance = ResendVerificationAuthRequest.from_json(json)
# print the JSON string representation of the object
print(ResendVerificationAuthRequest.to_json())

# convert the object into a dict
resend_verification_auth_request_dict = resend_verification_auth_request_instance.to_dict()
# create an instance of ResendVerificationAuthRequest from a dict
resend_verification_auth_request_from_dict = ResendVerificationAuthRequest.from_dict(resend_verification_auth_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


