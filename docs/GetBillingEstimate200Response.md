# GetBillingEstimate200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**period** | **str** | Current month YYYY-MM | [optional] 
**line_items** | [**List[GetBillingEstimate200ResponseLineItemsInner]**](GetBillingEstimate200ResponseLineItemsInner.md) |  | [optional] 
**estimated_overage_cents** | **float** |  | [optional] 
**estimated_overage** | **str** |  | [optional] 
**forecast_overage_cents** | **float** |  | [optional] 
**forecast_overage** | **str** |  | [optional] 
**message** | **str** | Human-readable forecast when applicable | [optional] 
**spend_limits** | [**GetBillingEstimate200ResponseSpendLimits**](GetBillingEstimate200ResponseSpendLimits.md) |  | [optional] 

## Example

```python
from mudbase.models.get_billing_estimate200_response import GetBillingEstimate200Response

# TODO update the JSON string below
json = "{}"
# create an instance of GetBillingEstimate200Response from a JSON string
get_billing_estimate200_response_instance = GetBillingEstimate200Response.from_json(json)
# print the JSON string representation of the object
print(GetBillingEstimate200Response.to_json())

# convert the object into a dict
get_billing_estimate200_response_dict = get_billing_estimate200_response_instance.to_dict()
# create an instance of GetBillingEstimate200Response from a dict
get_billing_estimate200_response_from_dict = GetBillingEstimate200Response.from_dict(get_billing_estimate200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


