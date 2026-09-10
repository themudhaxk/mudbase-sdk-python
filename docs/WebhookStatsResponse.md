# WebhookStatsResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**status_stats** | [**List[WebhookStatsResponseStatusStatsInner]**](WebhookStatsResponseStatusStatsInner.md) | Grouped by delivery status | 
**event_stats** | [**List[WebhookStatsResponseEventStatsInner]**](WebhookStatsResponseEventStatsInner.md) | Grouped by event name | 
**period** | **str** |  | 

## Example

```python
from mudbase.models.webhook_stats_response import WebhookStatsResponse

# TODO update the JSON string below
json = "{}"
# create an instance of WebhookStatsResponse from a JSON string
webhook_stats_response_instance = WebhookStatsResponse.from_json(json)
# print the JSON string representation of the object
print(WebhookStatsResponse.to_json())

# convert the object into a dict
webhook_stats_response_dict = webhook_stats_response_instance.to_dict()
# create an instance of WebhookStatsResponse from a dict
webhook_stats_response_from_dict = WebhookStatsResponse.from_dict(webhook_stats_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


