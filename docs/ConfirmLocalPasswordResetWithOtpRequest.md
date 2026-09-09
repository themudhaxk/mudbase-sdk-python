# ConfirmLocalPasswordResetWithOtpRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**email** | **str** |  | 
**project_id** | **str** |  | 
**otp** | **str** |  | 
**new_password** | **str** |  | 

## Example

```python
from mudbase.models.confirm_local_password_reset_with_otp_request import ConfirmLocalPasswordResetWithOtpRequest

# TODO update the JSON string below
json = "{}"
# create an instance of ConfirmLocalPasswordResetWithOtpRequest from a JSON string
confirm_local_password_reset_with_otp_request_instance = ConfirmLocalPasswordResetWithOtpRequest.from_json(json)
# print the JSON string representation of the object
print(ConfirmLocalPasswordResetWithOtpRequest.to_json())

# convert the object into a dict
confirm_local_password_reset_with_otp_request_dict = confirm_local_password_reset_with_otp_request_instance.to_dict()
# create an instance of ConfirmLocalPasswordResetWithOtpRequest from a dict
confirm_local_password_reset_with_otp_request_from_dict = ConfirmLocalPasswordResetWithOtpRequest.from_dict(confirm_local_password_reset_with_otp_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


