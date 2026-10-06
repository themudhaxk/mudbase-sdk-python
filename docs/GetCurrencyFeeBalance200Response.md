# GetCurrencyFeeBalance200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**success** | **bool** |  | [optional] 
**data** | [**GetCurrencyFeeBalance200ResponseData**](GetCurrencyFeeBalance200ResponseData.md) |  | [optional] 

## Example

```python
from mudbase.models.get_currency_fee_balance200_response import GetCurrencyFeeBalance200Response

# TODO update the JSON string below
json = "{}"
# create an instance of GetCurrencyFeeBalance200Response from a JSON string
get_currency_fee_balance200_response_instance = GetCurrencyFeeBalance200Response.from_json(json)
# print the JSON string representation of the object
print(GetCurrencyFeeBalance200Response.to_json())

# convert the object into a dict
get_currency_fee_balance200_response_dict = get_currency_fee_balance200_response_instance.to_dict()
# create an instance of GetCurrencyFeeBalance200Response from a dict
get_currency_fee_balance200_response_from_dict = GetCurrencyFeeBalance200Response.from_dict(get_currency_fee_balance200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


