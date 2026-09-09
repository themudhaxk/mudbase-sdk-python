# InitiateAddressVerification200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**success** | **bool** |  | [optional] 
**message** | **str** |  | [optional] 
**verification_status** | **str** |  | [optional] 

## Example

```python
from mudbase.models.initiate_address_verification200_response import InitiateAddressVerification200Response

# TODO update the JSON string below
json = "{}"
# create an instance of InitiateAddressVerification200Response from a JSON string
initiate_address_verification200_response_instance = InitiateAddressVerification200Response.from_json(json)
# print the JSON string representation of the object
print(InitiateAddressVerification200Response.to_json())

# convert the object into a dict
initiate_address_verification200_response_dict = initiate_address_verification200_response_instance.to_dict()
# create an instance of InitiateAddressVerification200Response from a dict
initiate_address_verification200_response_from_dict = InitiateAddressVerification200Response.from_dict(initiate_address_verification200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


