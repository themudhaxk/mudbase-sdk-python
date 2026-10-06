# GetBillingEstimate200ResponseSpendLimits


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**soft_limit_cents** | **float** |  | [optional] 
**hard_limit_cents** | **float** |  | [optional] 
**spend_blocked** | **bool** |  | [optional] 

## Example

```python
from mudbase.models.get_billing_estimate200_response_spend_limits import GetBillingEstimate200ResponseSpendLimits

# TODO update the JSON string below
json = "{}"
# create an instance of GetBillingEstimate200ResponseSpendLimits from a JSON string
get_billing_estimate200_response_spend_limits_instance = GetBillingEstimate200ResponseSpendLimits.from_json(json)
# print the JSON string representation of the object
print(GetBillingEstimate200ResponseSpendLimits.to_json())

# convert the object into a dict
get_billing_estimate200_response_spend_limits_dict = get_billing_estimate200_response_spend_limits_instance.to_dict()
# create an instance of GetBillingEstimate200ResponseSpendLimits from a dict
get_billing_estimate200_response_spend_limits_from_dict = GetBillingEstimate200ResponseSpendLimits.from_dict(get_billing_estimate200_response_spend_limits_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


