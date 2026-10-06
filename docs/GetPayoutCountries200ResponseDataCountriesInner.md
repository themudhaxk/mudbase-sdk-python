# GetPayoutCountries200ResponseDataCountriesInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**code** | **str** | ISO-3166 alpha-2 country code (e.g. NG, GH, KE, US, GB). | [optional] 
**name** | **str** |  | [optional] 
**currency** | **str** |  | [optional] 
**banks_list_supported** | **bool** | Whether GET /payment-processing/banks returns a live bank list for this country. | [optional] 
**mobile_money** | **bool** |  | [optional] 
**international** | **bool** | True for a market whose settlement rail requires an account-level capability beyond the standard local-rail onboarding (currently US, GB). | [optional] 
**fields** | [**List[GetPayoutCountries200ResponseDataCountriesInnerFieldsInner]**](GetPayoutCountries200ResponseDataCountriesInnerFieldsInner.md) |  | [optional] 

## Example

```python
from mudbase.models.get_payout_countries200_response_data_countries_inner import GetPayoutCountries200ResponseDataCountriesInner

# TODO update the JSON string below
json = "{}"
# create an instance of GetPayoutCountries200ResponseDataCountriesInner from a JSON string
get_payout_countries200_response_data_countries_inner_instance = GetPayoutCountries200ResponseDataCountriesInner.from_json(json)
# print the JSON string representation of the object
print(GetPayoutCountries200ResponseDataCountriesInner.to_json())

# convert the object into a dict
get_payout_countries200_response_data_countries_inner_dict = get_payout_countries200_response_data_countries_inner_instance.to_dict()
# create an instance of GetPayoutCountries200ResponseDataCountriesInner from a dict
get_payout_countries200_response_data_countries_inner_from_dict = GetPayoutCountries200ResponseDataCountriesInner.from_dict(get_payout_countries200_response_data_countries_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


