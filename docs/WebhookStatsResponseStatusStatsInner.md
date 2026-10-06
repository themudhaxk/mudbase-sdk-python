# WebhookStatsResponseStatusStatsInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** | Status key (pending, success, failed, retrying) | [optional] 
**count** | **int** |  | [optional] 
**avg_duration** | **float** | Average duration in ms for that status bucket | [optional] 

## Example

```python
from mudbase.models.webhook_stats_response_status_stats_inner import WebhookStatsResponseStatusStatsInner

# TODO update the JSON string below
json = "{}"
# create an instance of WebhookStatsResponseStatusStatsInner from a JSON string
webhook_stats_response_status_stats_inner_instance = WebhookStatsResponseStatusStatsInner.from_json(json)
# print the JSON string representation of the object
print(WebhookStatsResponseStatusStatsInner.to_json())

# convert the object into a dict
webhook_stats_response_status_stats_inner_dict = webhook_stats_response_status_stats_inner_instance.to_dict()
# create an instance of WebhookStatsResponseStatusStatsInner from a dict
webhook_stats_response_status_stats_inner_from_dict = WebhookStatsResponseStatusStatsInner.from_dict(webhook_stats_response_status_stats_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


