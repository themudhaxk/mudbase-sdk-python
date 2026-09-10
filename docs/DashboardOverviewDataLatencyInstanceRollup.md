# DashboardOverviewDataLatencyInstanceRollup

In-process p50/p95/p99 for this Node instance (ephemeral; multi-pod differs per replica)

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**scope** | **str** |  | [optional] 
**p50_ms** | **int** |  | [optional] 
**p95_ms** | **int** |  | [optional] 
**p99_ms** | **int** |  | [optional] 
**mean_ms** | **int** |  | [optional] 
**samples_approx** | **int** |  | [optional] 
**templates_tracked** | **int** |  | [optional] 

## Example

```python
from mudbase.models.dashboard_overview_data_latency_instance_rollup import DashboardOverviewDataLatencyInstanceRollup

# TODO update the JSON string below
json = "{}"
# create an instance of DashboardOverviewDataLatencyInstanceRollup from a JSON string
dashboard_overview_data_latency_instance_rollup_instance = DashboardOverviewDataLatencyInstanceRollup.from_json(json)
# print the JSON string representation of the object
print(DashboardOverviewDataLatencyInstanceRollup.to_json())

# convert the object into a dict
dashboard_overview_data_latency_instance_rollup_dict = dashboard_overview_data_latency_instance_rollup_instance.to_dict()
# create an instance of DashboardOverviewDataLatencyInstanceRollup from a dict
dashboard_overview_data_latency_instance_rollup_from_dict = DashboardOverviewDataLatencyInstanceRollup.from_dict(dashboard_overview_data_latency_instance_rollup_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


