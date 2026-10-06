# GetPaymentProcessingStatus200ResponseDataStablecoin

Status of the separate stablecoin payment-links surface for this org (see Payment Links).

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**enabled** | **bool** |  | [optional] 
**settlement_fiat** | **str** |  | [optional] 
**wallet_count** | **int** |  | [optional] 

## Example

```python
from mudbase.models.get_payment_processing_status200_response_data_stablecoin import GetPaymentProcessingStatus200ResponseDataStablecoin

# TODO update the JSON string below
json = "{}"
# create an instance of GetPaymentProcessingStatus200ResponseDataStablecoin from a JSON string
get_payment_processing_status200_response_data_stablecoin_instance = GetPaymentProcessingStatus200ResponseDataStablecoin.from_json(json)
# print the JSON string representation of the object
print(GetPaymentProcessingStatus200ResponseDataStablecoin.to_json())

# convert the object into a dict
get_payment_processing_status200_response_data_stablecoin_dict = get_payment_processing_status200_response_data_stablecoin_instance.to_dict()
# create an instance of GetPaymentProcessingStatus200ResponseDataStablecoin from a dict
get_payment_processing_status200_response_data_stablecoin_from_dict = GetPaymentProcessingStatus200ResponseDataStablecoin.from_dict(get_payment_processing_status200_response_data_stablecoin_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


