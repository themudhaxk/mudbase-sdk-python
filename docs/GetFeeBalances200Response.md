# GetFeeBalances200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**success** | **bool** |  | [optional] 
**data** | [**List[GetFeeBalances200ResponseDataInner]**](GetFeeBalances200ResponseDataInner.md) |  | [optional] 

## Example

```python
from mudbase.models.get_fee_balances200_response import GetFeeBalances200Response

# TODO update the JSON string below
json = "{}"
# create an instance of GetFeeBalances200Response from a JSON string
get_fee_balances200_response_instance = GetFeeBalances200Response.from_json(json)
# print the JSON string representation of the object
print(GetFeeBalances200Response.to_json())

# convert the object into a dict
get_fee_balances200_response_dict = get_fee_balances200_response_instance.to_dict()
# create an instance of GetFeeBalances200Response from a dict
get_fee_balances200_response_from_dict = GetFeeBalances200Response.from_dict(get_fee_balances200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


