# ConfirmAddressVerification200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**success** | **bool** |  | [optional] 
**message** | **str** |  | [optional] 
**verified** | **bool** |  | [optional] 
**verified_at** | **datetime** |  | [optional] 

## Example

```python
from mudbase.models.confirm_address_verification200_response import ConfirmAddressVerification200Response

# TODO update the JSON string below
json = "{}"
# create an instance of ConfirmAddressVerification200Response from a JSON string
confirm_address_verification200_response_instance = ConfirmAddressVerification200Response.from_json(json)
# print the JSON string representation of the object
print(ConfirmAddressVerification200Response.to_json())

# convert the object into a dict
confirm_address_verification200_response_dict = confirm_address_verification200_response_instance.to_dict()
# create an instance of ConfirmAddressVerification200Response from a dict
confirm_address_verification200_response_from_dict = ConfirmAddressVerification200Response.from_dict(confirm_address_verification200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


