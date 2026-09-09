# EnablePaymentProcessing200ResponseData


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**subaccount_id** | **str** |  | [optional] 
**already_enabled** | **bool** |  | [optional] 

## Example

```python
from mudbase.models.enable_payment_processing200_response_data import EnablePaymentProcessing200ResponseData

# TODO update the JSON string below
json = "{}"
# create an instance of EnablePaymentProcessing200ResponseData from a JSON string
enable_payment_processing200_response_data_instance = EnablePaymentProcessing200ResponseData.from_json(json)
# print the JSON string representation of the object
print(EnablePaymentProcessing200ResponseData.to_json())

# convert the object into a dict
enable_payment_processing200_response_data_dict = enable_payment_processing200_response_data_instance.to_dict()
# create an instance of EnablePaymentProcessing200ResponseData from a dict
enable_payment_processing200_response_data_from_dict = EnablePaymentProcessing200ResponseData.from_dict(enable_payment_processing200_response_data_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


