# ApiGdprErasePostRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**confirm** | **str** | Must equal \&quot;DELETE\&quot; to proceed with erasure. | 
**current_password** | **str** | Required unless the account has no password set (OAuth-only) | [optional] 
**totp_token** | **str** | Required only if the account has 2FA enabled | [optional] 

## Example

```python
from mudbase.models.api_gdpr_erase_post_request import ApiGdprErasePostRequest

# TODO update the JSON string below
json = "{}"
# create an instance of ApiGdprErasePostRequest from a JSON string
api_gdpr_erase_post_request_instance = ApiGdprErasePostRequest.from_json(json)
# print the JSON string representation of the object
print(ApiGdprErasePostRequest.to_json())

# convert the object into a dict
api_gdpr_erase_post_request_dict = api_gdpr_erase_post_request_instance.to_dict()
# create an instance of ApiGdprErasePostRequest from a dict
api_gdpr_erase_post_request_from_dict = ApiGdprErasePostRequest.from_dict(api_gdpr_erase_post_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


