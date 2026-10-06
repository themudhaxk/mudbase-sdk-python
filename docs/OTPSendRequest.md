# OTPSendRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**phone** | **str** |  | [optional] 
**email** | **str** |  | [optional] 
**project_id** | **str** |  | 
**method** | **str** |  | 

## Example

```python
from mudbase.models.otp_send_request import OTPSendRequest

# TODO update the JSON string below
json = "{}"
# create an instance of OTPSendRequest from a JSON string
otp_send_request_instance = OTPSendRequest.from_json(json)
# print the JSON string representation of the object
print(OTPSendRequest.to_json())

# convert the object into a dict
otp_send_request_dict = otp_send_request_instance.to_dict()
# create an instance of OTPSendRequest from a dict
otp_send_request_from_dict = OTPSendRequest.from_dict(otp_send_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


