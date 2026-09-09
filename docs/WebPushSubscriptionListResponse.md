# WebPushSubscriptionListResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**success** | **bool** |  | [optional] 
**data** | [**List[WebPushSubscriptionSummary]**](WebPushSubscriptionSummary.md) |  | [optional] 

## Example

```python
from mudbase.models.web_push_subscription_list_response import WebPushSubscriptionListResponse

# TODO update the JSON string below
json = "{}"
# create an instance of WebPushSubscriptionListResponse from a JSON string
web_push_subscription_list_response_instance = WebPushSubscriptionListResponse.from_json(json)
# print the JSON string representation of the object
print(WebPushSubscriptionListResponse.to_json())

# convert the object into a dict
web_push_subscription_list_response_dict = web_push_subscription_list_response_instance.to_dict()
# create an instance of WebPushSubscriptionListResponse from a dict
web_push_subscription_list_response_from_dict = WebPushSubscriptionListResponse.from_dict(web_push_subscription_list_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


