# ApiKycWebhookConfigTestPost200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ok** | **bool** |  | [optional] 
**http_status** | **int** |  | [optional] 
**error** | **str** |  | [optional] 

## Example

```python
from mudbase.models.api_kyc_webhook_config_test_post200_response import ApiKycWebhookConfigTestPost200Response

# TODO update the JSON string below
json = "{}"
# create an instance of ApiKycWebhookConfigTestPost200Response from a JSON string
api_kyc_webhook_config_test_post200_response_instance = ApiKycWebhookConfigTestPost200Response.from_json(json)
# print the JSON string representation of the object
print(ApiKycWebhookConfigTestPost200Response.to_json())

# convert the object into a dict
api_kyc_webhook_config_test_post200_response_dict = api_kyc_webhook_config_test_post200_response_instance.to_dict()
# create an instance of ApiKycWebhookConfigTestPost200Response from a dict
api_kyc_webhook_config_test_post200_response_from_dict = ApiKycWebhookConfigTestPost200Response.from_dict(api_kyc_webhook_config_test_post200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


