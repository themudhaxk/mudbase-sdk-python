# GetSubscriptionTiers200ResponsePlansInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** |  | [optional] 
**name** | **str** |  | [optional] 
**description** | **str** |  | [optional] 
**price** | **float** | Monthly price in cents | [optional] 
**price_yearly** | **float** | Yearly price in cents (2 months free, ~16.67% off) | [optional] 
**currency** | **str** |  | [optional] 
**price_id** | **str** |  | [optional] 
**limits** | **object** |  | [optional] 
**overages** | **object** |  | [optional] 
**enforcement** | **object** | Per-resource enforcement (blocking, billing_only, etc.) | [optional] 

## Example

```python
from mudbase.models.get_subscription_tiers200_response_plans_inner import GetSubscriptionTiers200ResponsePlansInner

# TODO update the JSON string below
json = "{}"
# create an instance of GetSubscriptionTiers200ResponsePlansInner from a JSON string
get_subscription_tiers200_response_plans_inner_instance = GetSubscriptionTiers200ResponsePlansInner.from_json(json)
# print the JSON string representation of the object
print(GetSubscriptionTiers200ResponsePlansInner.to_json())

# convert the object into a dict
get_subscription_tiers200_response_plans_inner_dict = get_subscription_tiers200_response_plans_inner_instance.to_dict()
# create an instance of GetSubscriptionTiers200ResponsePlansInner from a dict
get_subscription_tiers200_response_plans_inner_from_dict = GetSubscriptionTiers200ResponsePlansInner.from_dict(get_subscription_tiers200_response_plans_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


