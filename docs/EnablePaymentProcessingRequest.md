# EnablePaymentProcessingRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_bank** | **str** | Bank code (from GET /v3/banks/{country}) | 
**account_number** | **str** | Org bank account number | 
**country** | **str** | Country code (e.g. US, NG) | 
**business_name** | **str** |  | 
**business_mobile** | **str** |  | [optional] 
**bvn** | **str** | Required only when country is NG (Nigeria) | [optional] 

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


