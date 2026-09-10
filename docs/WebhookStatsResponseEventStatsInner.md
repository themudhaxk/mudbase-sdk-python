# WebhookStatsResponseEventStatsInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** | Event name | [optional] 
**count** | **int** |  | [optional] 
**success_rate** | **float** | Fraction of logs with status success (0–1) | [optional] 

## Example

```python
from mudbase.models.webhook_stats_response_event_stats_inner import WebhookStatsResponseEventStatsInner

# TODO update the JSON string below
json = "{}"
# create an instance of WebhookStatsResponseEventStatsInner from a JSON string
webhook_stats_response_event_stats_inner_instance = WebhookStatsResponseEventStatsInner.from_json(json)
# print the JSON string representation of the object
print(WebhookStatsResponseEventStatsInner.to_json())

# convert the object into a dict
webhook_stats_response_event_stats_inner_dict = webhook_stats_response_event_stats_inner_instance.to_dict()
# create an instance of WebhookStatsResponseEventStatsInner from a dict
webhook_stats_response_event_stats_inner_from_dict = WebhookStatsResponseEventStatsInner.from_dict(webhook_stats_response_event_stats_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


