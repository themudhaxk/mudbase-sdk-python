# GetPayoutCountries200ResponseData


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**countries** | [**List[GetPayoutCountries200ResponseDataCountriesInner]**](GetPayoutCountries200ResponseDataCountriesInner.md) |  | [optional] 

## Example

```python
from mudbase.models.get_payout_countries200_response_data import GetPayoutCountries200ResponseData

# TODO update the JSON string below
json = "{}"
# create an instance of GetPayoutCountries200ResponseData from a JSON string
get_payout_countries200_response_data_instance = GetPayoutCountries200ResponseData.from_json(json)
# print the JSON string representation of the object
print(GetPayoutCountries200ResponseData.to_json())

# convert the object into a dict
get_payout_countries200_response_data_dict = get_payout_countries200_response_data_instance.to_dict()
# create an instance of GetPayoutCountries200ResponseData from a dict
get_payout_countries200_response_data_from_dict = GetPayoutCountries200ResponseData.from_dict(get_payout_countries200_response_data_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


