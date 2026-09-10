# WebPushSubscription

A browser `PushSubscription` from `pushManager.subscribe()` - the push-service `endpoint` plus the `p256dh` / `auth` keys the server needs to encrypt a payload for that endpoint. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**endpoint** | **str** | The push-service endpoint URL returned by &#x60;pushManager.subscribe()&#x60;. | 
**keys** | [**WebPushSubscriptionKeys**](WebPushSubscriptionKeys.md) |  | 

## Example

```python
from mudbase.models.web_push_subscription import WebPushSubscription

# TODO update the JSON string below
json = "{}"
# create an instance of WebPushSubscription from a JSON string
web_push_subscription_instance = WebPushSubscription.from_json(json)
# print the JSON string representation of the object
print(WebPushSubscription.to_json())

# convert the object into a dict
web_push_subscription_dict = web_push_subscription_instance.to_dict()
# create an instance of WebPushSubscription from a dict
web_push_subscription_from_dict = WebPushSubscription.from_dict(web_push_subscription_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


