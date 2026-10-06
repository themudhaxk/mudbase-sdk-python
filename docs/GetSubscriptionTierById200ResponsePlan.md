# GetSubscriptionTierById200ResponsePlan


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** |  | [optional] 
**name** | **str** |  | [optional] 
**description** | **str** |  | [optional] 
**price** | **float** |  | [optional] 
**price_yearly** | **float** |  | [optional] 
**currency** | **str** |  | [optional] 
**limits** | **object** |  | [optional] 
**overages** | **object** |  | [optional] 

## Example

```python
from mudbase.models.get_subscription_tier_by_id200_response_plan import GetSubscriptionTierById200ResponsePlan

# TODO update the JSON string below
json = "{}"
# create an instance of GetSubscriptionTierById200ResponsePlan from a JSON string
get_subscription_tier_by_id200_response_plan_instance = GetSubscriptionTierById200ResponsePlan.from_json(json)
# print the JSON string representation of the object
print(GetSubscriptionTierById200ResponsePlan.to_json())

# convert the object into a dict
get_subscription_tier_by_id200_response_plan_dict = get_subscription_tier_by_id200_response_plan_instance.to_dict()
# create an instance of GetSubscriptionTierById200ResponsePlan from a dict
get_subscription_tier_by_id200_response_plan_from_dict = GetSubscriptionTierById200ResponsePlan.from_dict(get_subscription_tier_by_id200_response_plan_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


