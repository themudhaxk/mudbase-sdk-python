# WebPushSubscriptionSummary

A registered Web Push subscription. The encryption keys are never returned.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**endpoint** | **str** |  | [optional] 
**user_id** | **str** |  | [optional] 
**device_id** | **str** |  | [optional] 
**user_agent** | **str** |  | [optional] 
**disabled** | **bool** |  | [optional] 
**last_seen_at** | **datetime** |  | [optional] 
**created_at** | **datetime** |  | [optional] 

## Example

```python
from mudbase.models.web_push_subscription_summary import WebPushSubscriptionSummary

# TODO update the JSON string below
json = "{}"
# create an instance of WebPushSubscriptionSummary from a JSON string
web_push_subscription_summary_instance = WebPushSubscriptionSummary.from_json(json)
# print the JSON string representation of the object
print(WebPushSubscriptionSummary.to_json())

# convert the object into a dict
web_push_subscription_summary_dict = web_push_subscription_summary_instance.to_dict()
# create an instance of WebPushSubscriptionSummary from a dict
web_push_subscription_summary_from_dict = WebPushSubscriptionSummary.from_dict(web_push_subscription_summary_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


