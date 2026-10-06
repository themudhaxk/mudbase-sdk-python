# GetCurrencyFeeBalance200ResponseData


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**currency** | **str** |  | [optional] 
**collected_amount** | **float** |  | [optional] 
**threshold** | **float** |  | [optional] 
**status** | **str** |  | [optional] 

## Example

```python
from mudbase.models.get_currency_fee_balance200_response_data import GetCurrencyFeeBalance200ResponseData

# TODO update the JSON string below
json = "{}"
# create an instance of GetCurrencyFeeBalance200ResponseData from a JSON string
get_currency_fee_balance200_response_data_instance = GetCurrencyFeeBalance200ResponseData.from_json(json)
# print the JSON string representation of the object
print(GetCurrencyFeeBalance200ResponseData.to_json())

# convert the object into a dict
get_currency_fee_balance200_response_data_dict = get_currency_fee_balance200_response_data_instance.to_dict()
# create an instance of GetCurrencyFeeBalance200ResponseData from a dict
get_currency_fee_balance200_response_data_from_dict = GetCurrencyFeeBalance200ResponseData.from_dict(get_currency_fee_balance200_response_data_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


