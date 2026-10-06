# OTPVerifyRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**identifier** | **str** |  | [optional] 
**otp** | **str** |  | 
**project_id** | **str** |  | 

## Example

```python
from mudbase.models.otp_verify_request import OTPVerifyRequest

# TODO update the JSON string below
json = "{}"
# create an instance of OTPVerifyRequest from a JSON string
otp_verify_request_instance = OTPVerifyRequest.from_json(json)
# print the JSON string representation of the object
print(OTPVerifyRequest.to_json())

# convert the object into a dict
otp_verify_request_dict = otp_verify_request_instance.to_dict()
# create an instance of OTPVerifyRequest from a dict
otp_verify_request_from_dict = OTPVerifyRequest.from_dict(otp_verify_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


