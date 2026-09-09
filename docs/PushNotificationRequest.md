# PushNotificationRequest

Provide at least one target: `tokens` (registered device tokens), `endpoints` (registered Web Push subscription endpoints), `userIds` (Web Push subscriptions associated to those user ids), or `webPushBroadcast: true` (every enabled Web Push subscription in the project). A single send can target both the device-token channel and the native Web Push channel at once. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**tokens** | **List[str]** | Registered device push tokens to deliver to (device-token channel). | [optional] 
**endpoints** | **List[str]** | Registered Web Push subscription endpoints to deliver to (native Web Push channel).  | [optional] 
**user_ids** | **List[str]** | Deliver to every Web Push subscription registered under these user ids (native Web Push channel).  | [optional] 
**web_push_broadcast** | **bool** | When true, deliver to every enabled Web Push subscription registered to the project (native Web Push channel). Ignored when the project has not enabled native Web Push.  | [optional] 
**title** | **str** |  | 
**body** | **str** |  | 
**data** | **object** |  | [optional] 
**image_url** | **str** |  | [optional] 

## Example

```python
from mudbase.models.push_notification_request import PushNotificationRequest

# TODO update the JSON string below
json = "{}"
# create an instance of PushNotificationRequest from a JSON string
push_notification_request_instance = PushNotificationRequest.from_json(json)
# print the JSON string representation of the object
print(PushNotificationRequest.to_json())

# convert the object into a dict
push_notification_request_dict = push_notification_request_instance.to_dict()
# create an instance of PushNotificationRequest from a dict
push_notification_request_from_dict = PushNotificationRequest.from_dict(push_notification_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


