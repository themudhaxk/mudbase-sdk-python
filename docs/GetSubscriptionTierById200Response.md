# GetSubscriptionTierById200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**plan** | [**GetSubscriptionTierById200ResponsePlan**](GetSubscriptionTierById200ResponsePlan.md) |  | [optional] 

## Example

```python
from mudbase.models.get_subscription_tier_by_id200_response import GetSubscriptionTierById200Response

# TODO update the JSON string below
json = "{}"
# create an instance of GetSubscriptionTierById200Response from a JSON string
get_subscription_tier_by_id200_response_instance = GetSubscriptionTierById200Response.from_json(json)
# print the JSON string representation of the object
print(GetSubscriptionTierById200Response.to_json())

# convert the object into a dict
get_subscription_tier_by_id200_response_dict = get_subscription_tier_by_id200_response_instance.to_dict()
# create an instance of GetSubscriptionTierById200Response from a dict
get_subscription_tier_by_id200_response_from_dict = GetSubscriptionTierById200Response.from_dict(get_subscription_tier_by_id200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


