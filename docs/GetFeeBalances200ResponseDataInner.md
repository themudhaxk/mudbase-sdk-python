# GetFeeBalances200ResponseDataInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**currency** | **str** |  | [optional] 
**collected_amount** | **float** |  | [optional] 
**threshold** | **float** |  | [optional] 
**status** | **str** |  | [optional] 
**total_collected** | **float** |  | [optional] 
**total_paid_out** | **float** |  | [optional] 

## Example

```python
from mudbase.models.get_fee_balances200_response_data_inner import GetFeeBalances200ResponseDataInner

# TODO update the JSON string below
json = "{}"
# create an instance of GetFeeBalances200ResponseDataInner from a JSON string
get_fee_balances200_response_data_inner_instance = GetFeeBalances200ResponseDataInner.from_json(json)
# print the JSON string representation of the object
print(GetFeeBalances200ResponseDataInner.to_json())

# convert the object into a dict
get_fee_balances200_response_data_inner_dict = get_fee_balances200_response_data_inner_instance.to_dict()
# create an instance of GetFeeBalances200ResponseDataInner from a dict
get_fee_balances200_response_data_inner_from_dict = GetFeeBalances200ResponseDataInner.from_dict(get_fee_balances200_response_data_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


