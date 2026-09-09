# TwoFASetupResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**secret** | **str** |  | [optional] 
**qr_code** | **str** |  | [optional] 
**manual_entry_key** | **str** |  | [optional] 

## Example

```python
from mudbase.models.two_fa_setup_response import TwoFASetupResponse

# TODO update the JSON string below
json = "{}"
# create an instance of TwoFASetupResponse from a JSON string
two_fa_setup_response_instance = TwoFASetupResponse.from_json(json)
# print the JSON string representation of the object
print(TwoFASetupResponse.to_json())

# convert the object into a dict
two_fa_setup_response_dict = two_fa_setup_response_instance.to_dict()
# create an instance of TwoFASetupResponse from a dict
two_fa_setup_response_from_dict = TwoFASetupResponse.from_dict(two_fa_setup_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


