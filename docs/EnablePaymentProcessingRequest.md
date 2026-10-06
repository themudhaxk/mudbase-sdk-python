# EnablePaymentProcessingRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**country** | **str** | ISO-3166 alpha-2 payout country code, one of the codes returned by GET /payment-processing/countries (e.g. NG, GH, KE, US, GB). | 
**business_name** | **str** |  | 
**business_mobile** | **str** | Optional, used for payout provider account notifications. | [optional] 
**account_bank** | **str** | Bank code, mobile-money network code, routing number, or sort code, depending on country. | [optional] 
**account_number** | **str** | Bank/mobile-money account number, IBAN, or similar, depending on country. | [optional] 
**bvn** | **str** | Required only when country is NG (Nigeria). | [optional] 
**account_type** | **str** | Required only when country is US (checking or savings). | [optional] 
**account_holder_name** | **str** | Required only when country is US or GB. | [optional] 

## Example

```python
from mudbase.models.enable_payment_processing_request import EnablePaymentProcessingRequest

# TODO update the JSON string below
json = "{}"
# create an instance of EnablePaymentProcessingRequest from a JSON string
enable_payment_processing_request_instance = EnablePaymentProcessingRequest.from_json(json)
# print the JSON string representation of the object
print(EnablePaymentProcessingRequest.to_json())

# convert the object into a dict
enable_payment_processing_request_dict = enable_payment_processing_request_instance.to_dict()
# create an instance of EnablePaymentProcessingRequest from a dict
enable_payment_processing_request_from_dict = EnablePaymentProcessingRequest.from_dict(enable_payment_processing_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


