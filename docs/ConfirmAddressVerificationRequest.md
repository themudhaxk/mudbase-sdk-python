# ConfirmAddressVerificationRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**tx_hash** | **str** |  | 

## Example

```python
from mudbase.models.confirm_address_verification_request import ConfirmAddressVerificationRequest

# TODO update the JSON string below
json = "{}"
# create an instance of ConfirmAddressVerificationRequest from a JSON string
confirm_address_verification_request_instance = ConfirmAddressVerificationRequest.from_json(json)
# print the JSON string representation of the object
print(ConfirmAddressVerificationRequest.to_json())

# convert the object into a dict
confirm_address_verification_request_dict = confirm_address_verification_request_instance.to_dict()
# create an instance of ConfirmAddressVerificationRequest from a dict
confirm_address_verification_request_from_dict = ConfirmAddressVerificationRequest.from_dict(confirm_address_verification_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


