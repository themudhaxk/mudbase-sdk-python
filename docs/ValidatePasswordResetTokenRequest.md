# ValidatePasswordResetTokenRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**token** | **str** | Token from the reset link query parameter | 

## Example

```python
from mudbase.models.validate_password_reset_token_request import ValidatePasswordResetTokenRequest

# TODO update the JSON string below
json = "{}"
# create an instance of ValidatePasswordResetTokenRequest from a JSON string
validate_password_reset_token_request_instance = ValidatePasswordResetTokenRequest.from_json(json)
# print the JSON string representation of the object
print(ValidatePasswordResetTokenRequest.to_json())

# convert the object into a dict
validate_password_reset_token_request_dict = validate_password_reset_token_request_instance.to_dict()
# create an instance of ValidatePasswordResetTokenRequest from a dict
validate_password_reset_token_request_from_dict = ValidatePasswordResetTokenRequest.from_dict(validate_password_reset_token_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


