# GetPayoutHistory200ResponseDataInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** |  | [optional] 
**currency** | **str** |  | [optional] 
**gross_amount** | **float** |  | [optional] 
**network_fee** | **float** |  | [optional] 
**net_amount** | **float** |  | [optional] 
**to_address** | **str** |  | [optional] 
**tx_hash** | **str** |  | [optional] 
**status** | **str** |  | [optional] 
**created_at** | **datetime** |  | [optional] 

## Example

```python
from mudbase.models.get_payout_history200_response_data_inner import GetPayoutHistory200ResponseDataInner

# TODO update the JSON string below
json = "{}"
# create an instance of GetPayoutHistory200ResponseDataInner from a JSON string
get_payout_history200_response_data_inner_instance = GetPayoutHistory200ResponseDataInner.from_json(json)
# print the JSON string representation of the object
print(GetPayoutHistory200ResponseDataInner.to_json())

# convert the object into a dict
get_payout_history200_response_data_inner_dict = get_payout_history200_response_data_inner_instance.to_dict()
# create an instance of GetPayoutHistory200ResponseDataInner from a dict
get_payout_history200_response_data_inner_from_dict = GetPayoutHistory200ResponseDataInner.from_dict(get_payout_history200_response_data_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


