# ApiKycWebhookConfigPutRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**webhook_url** | **str** | Destination URL. Send null or empty string to clear. | [optional] 
**webhook_secret** | **str** | Explicit signing secret (min 16 chars). Send null or empty string to clear. | [optional] 
**generate_secret** | **bool** | When true, the server generates a new secret and returns it once. | [optional] 

## Example

```python
from mudbase.models.api_kyc_webhook_config_put_request import ApiKycWebhookConfigPutRequest

# TODO update the JSON string below
json = "{}"
# create an instance of ApiKycWebhookConfigPutRequest from a JSON string
api_kyc_webhook_config_put_request_instance = ApiKycWebhookConfigPutRequest.from_json(json)
# print the JSON string representation of the object
print(ApiKycWebhookConfigPutRequest.to_json())

# convert the object into a dict
api_kyc_webhook_config_put_request_dict = api_kyc_webhook_config_put_request_instance.to_dict()
# create an instance of ApiKycWebhookConfigPutRequest from a dict
api_kyc_webhook_config_put_request_from_dict = ApiKycWebhookConfigPutRequest.from_dict(api_kyc_webhook_config_put_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


