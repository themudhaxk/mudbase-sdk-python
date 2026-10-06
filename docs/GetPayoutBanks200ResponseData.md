# GetPayoutBanks200ResponseData


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**banks_list_supported** | **bool** |  | [optional] 
**banks** | [**List[GetPayoutBanks200ResponseDataBanksInner]**](GetPayoutBanks200ResponseDataBanksInner.md) |  | [optional] 

## Example

```python
from mudbase.models.get_payout_banks200_response_data import GetPayoutBanks200ResponseData

# TODO update the JSON string below
json = "{}"
# create an instance of GetPayoutBanks200ResponseData from a JSON string
get_payout_banks200_response_data_instance = GetPayoutBanks200ResponseData.from_json(json)
# print the JSON string representation of the object
print(GetPayoutBanks200ResponseData.to_json())

# convert the object into a dict
get_payout_banks200_response_data_dict = get_payout_banks200_response_data_instance.to_dict()
# create an instance of GetPayoutBanks200ResponseData from a dict
get_payout_banks200_response_data_from_dict = GetPayoutBanks200ResponseData.from_dict(get_payout_banks200_response_data_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


