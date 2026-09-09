# ApiKycSessionsPostRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**language** | **str** | Optional ISO language code for the verification UI. | [optional] 

## Example

```python
from mudbase.models.api_kyc_sessions_post_request import ApiKycSessionsPostRequest

# TODO update the JSON string below
json = "{}"
# create an instance of ApiKycSessionsPostRequest from a JSON string
api_kyc_sessions_post_request_instance = ApiKycSessionsPostRequest.from_json(json)
# print the JSON string representation of the object
print(ApiKycSessionsPostRequest.to_json())

# convert the object into a dict
api_kyc_sessions_post_request_dict = api_kyc_sessions_post_request_instance.to_dict()
# create an instance of ApiKycSessionsPostRequest from a dict
api_kyc_sessions_post_request_from_dict = ApiKycSessionsPostRequest.from_dict(api_kyc_sessions_post_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


