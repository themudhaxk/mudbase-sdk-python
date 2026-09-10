# WebPushSubscriptionKeys


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**p256dh** | **str** | The subscription&#39;s P-256 ECDH public key (base64url). | 
**auth** | **str** | The subscription&#39;s auth secret (base64url). | 

## Example

```python
from mudbase.models.web_push_subscription_keys import WebPushSubscriptionKeys

# TODO update the JSON string below
json = "{}"
# create an instance of WebPushSubscriptionKeys from a JSON string
web_push_subscription_keys_instance = WebPushSubscriptionKeys.from_json(json)
# print the JSON string representation of the object
print(WebPushSubscriptionKeys.to_json())

# convert the object into a dict
web_push_subscription_keys_dict = web_push_subscription_keys_instance.to_dict()
# create an instance of WebPushSubscriptionKeys from a dict
web_push_subscription_keys_from_dict = WebPushSubscriptionKeys.from_dict(web_push_subscription_keys_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


