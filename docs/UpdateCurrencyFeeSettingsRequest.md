# UpdateCurrencyFeeSettingsRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**enabled** | **bool** |  | [optional] 
**fee_amount** | **float** |  | [optional] 
**payout_address** | **str** |  | [optional] 
**payout_threshold** | **float** |  | [optional] 

## Example

```python
from mudbase.models.update_currency_fee_settings_request import UpdateCurrencyFeeSettingsRequest

# TODO update the JSON string below
json = "{}"
# create an instance of UpdateCurrencyFeeSettingsRequest from a JSON string
update_currency_fee_settings_request_instance = UpdateCurrencyFeeSettingsRequest.from_json(json)
# print the JSON string representation of the object
print(UpdateCurrencyFeeSettingsRequest.to_json())

# convert the object into a dict
update_currency_fee_settings_request_dict = update_currency_fee_settings_request_instance.to_dict()
# create an instance of UpdateCurrencyFeeSettingsRequest from a dict
update_currency_fee_settings_request_from_dict = UpdateCurrencyFeeSettingsRequest.from_dict(update_currency_fee_settings_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


