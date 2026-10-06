# ValidatePasswordResetToken400Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**valid** | **bool** |  | [optional] 
**error** | **str** |  | [optional] 

## Example

```python
from mudbase.models.validate_password_reset_token400_response import ValidatePasswordResetToken400Response

# TODO update the JSON string below
json = "{}"
# create an instance of ValidatePasswordResetToken400Response from a JSON string
validate_password_reset_token400_response_instance = ValidatePasswordResetToken400Response.from_json(json)
# print the JSON string representation of the object
print(ValidatePasswordResetToken400Response.to_json())

# convert the object into a dict
validate_password_reset_token400_response_dict = validate_password_reset_token400_response_instance.to_dict()
# create an instance of ValidatePasswordResetToken400Response from a dict
validate_password_reset_token400_response_from_dict = ValidatePasswordResetToken400Response.from_dict(validate_password_reset_token400_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


