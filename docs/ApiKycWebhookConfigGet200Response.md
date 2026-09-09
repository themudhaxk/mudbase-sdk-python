# ApiKycWebhookConfigGet200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**webhook_url** | **str** |  | [optional] 
**secret_set** | **bool** |  | [optional] 

## Example

```python
from mudbase.models.api_kyc_webhook_config_get200_response import ApiKycWebhookConfigGet200Response

# TODO update the JSON string below
json = "{}"
# create an instance of ApiKycWebhookConfigGet200Response from a JSON string
api_kyc_webhook_config_get200_response_instance = ApiKycWebhookConfigGet200Response.from_json(json)
# print the JSON string representation of the object
print(ApiKycWebhookConfigGet200Response.to_json())

# convert the object into a dict
api_kyc_webhook_config_get200_response_dict = api_kyc_webhook_config_get200_response_instance.to_dict()
# create an instance of ApiKycWebhookConfigGet200Response from a dict
api_kyc_webhook_config_get200_response_from_dict = ApiKycWebhookConfigGet200Response.from_dict(api_kyc_webhook_config_get200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


