# GetPayoutBanks200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**success** | **bool** |  | [optional] 
**data** | [**GetPayoutBanks200ResponseData**](GetPayoutBanks200ResponseData.md) |  | [optional] 

## Example

```python
from mudbase.models.get_payout_banks200_response import GetPayoutBanks200Response

# TODO update the JSON string below
json = "{}"
# create an instance of GetPayoutBanks200Response from a JSON string
get_payout_banks200_response_instance = GetPayoutBanks200Response.from_json(json)
# print the JSON string representation of the object
print(GetPayoutBanks200Response.to_json())

# convert the object into a dict
get_payout_banks200_response_dict = get_payout_banks200_response_instance.to_dict()
# create an instance of GetPayoutBanks200Response from a dict
get_payout_banks200_response_from_dict = GetPayoutBanks200Response.from_dict(get_payout_banks200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


