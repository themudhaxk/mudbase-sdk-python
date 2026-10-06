# GetPaymentProcessingStatus200ResponseData


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**onboarded** | **bool** |  | [optional] 
**enabled** | **bool** | Whether payment collection is actually toggled on (implies approved). | [optional] 
**approval_status** | **str** | not_submitted, pending_review, approved, or rejected. | [optional] 
**status** | **str** | Derived overall status for the console to render: not_onboarded, pending_review, rejected, disabled, or active. | [optional] 
**rejection_reason** | **str** |  | [optional] 
**stablecoin** | [**GetPaymentProcessingStatus200ResponseDataStablecoin**](GetPaymentProcessingStatus200ResponseDataStablecoin.md) |  | [optional] 

## Example

```python
from mudbase.models.get_payment_processing_status200_response_data import GetPaymentProcessingStatus200ResponseData

# TODO update the JSON string below
json = "{}"
# create an instance of GetPaymentProcessingStatus200ResponseData from a JSON string
get_payment_processing_status200_response_data_instance = GetPaymentProcessingStatus200ResponseData.from_json(json)
# print the JSON string representation of the object
print(GetPaymentProcessingStatus200ResponseData.to_json())

# convert the object into a dict
get_payment_processing_status200_response_data_dict = get_payment_processing_status200_response_data_instance.to_dict()
# create an instance of GetPaymentProcessingStatus200ResponseData from a dict
get_payment_processing_status200_response_data_from_dict = GetPaymentProcessingStatus200ResponseData.from_dict(get_payment_processing_status200_response_data_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


