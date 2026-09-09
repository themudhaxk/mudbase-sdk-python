# GetBillingEstimate200ResponseLineItemsInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**resource** | **str** |  | [optional] 
**units** | **float** |  | [optional] 
**amount** | **float** |  | [optional] 
**currency** | **str** |  | [optional] 
**unit** | **str** |  | [optional] 

## Example

```python
from mudbase.models.get_billing_estimate200_response_line_items_inner import GetBillingEstimate200ResponseLineItemsInner

# TODO update the JSON string below
json = "{}"
# create an instance of GetBillingEstimate200ResponseLineItemsInner from a JSON string
get_billing_estimate200_response_line_items_inner_instance = GetBillingEstimate200ResponseLineItemsInner.from_json(json)
# print the JSON string representation of the object
print(GetBillingEstimate200ResponseLineItemsInner.to_json())

# convert the object into a dict
get_billing_estimate200_response_line_items_inner_dict = get_billing_estimate200_response_line_items_inner_instance.to_dict()
# create an instance of GetBillingEstimate200ResponseLineItemsInner from a dict
get_billing_estimate200_response_line_items_inner_from_dict = GetBillingEstimate200ResponseLineItemsInner.from_dict(get_billing_estimate200_response_line_items_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


