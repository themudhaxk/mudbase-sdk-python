# EraseUserDataRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**confirm** | **str** |  | 
**current_password** | **str** | Required unless the account has no password set (OAuth-only) | [optional] 
**totp_token** | **str** | Required only if the account has 2FA enabled | [optional] 

## Example

```python
from mudbase.models.erase_user_data_request import EraseUserDataRequest

# TODO update the JSON string below
json = "{}"
# create an instance of EraseUserDataRequest from a JSON string
erase_user_data_request_instance = EraseUserDataRequest.from_json(json)
# print the JSON string representation of the object
print(EraseUserDataRequest.to_json())

# convert the object into a dict
erase_user_data_request_dict = erase_user_data_request_instance.to_dict()
# create an instance of EraseUserDataRequest from a dict
erase_user_data_request_from_dict = EraseUserDataRequest.from_dict(erase_user_data_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


