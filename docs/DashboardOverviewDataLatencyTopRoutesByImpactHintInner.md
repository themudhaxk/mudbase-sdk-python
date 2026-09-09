# DashboardOverviewDataLatencyTopRoutesByImpactHintInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**route_key** | **str** |  | [optional] 
**p50_ms** | **int** |  | [optional] 
**p95_ms** | **int** |  | [optional] 
**count** | **int** |  | [optional] 
**impact_score** | **int** |  | [optional] 

## Example

```python
from mudbase.models.dashboard_overview_data_latency_top_routes_by_impact_hint_inner import DashboardOverviewDataLatencyTopRoutesByImpactHintInner

# TODO update the JSON string below
json = "{}"
# create an instance of DashboardOverviewDataLatencyTopRoutesByImpactHintInner from a JSON string
dashboard_overview_data_latency_top_routes_by_impact_hint_inner_instance = DashboardOverviewDataLatencyTopRoutesByImpactHintInner.from_json(json)
# print the JSON string representation of the object
print(DashboardOverviewDataLatencyTopRoutesByImpactHintInner.to_json())

# convert the object into a dict
dashboard_overview_data_latency_top_routes_by_impact_hint_inner_dict = dashboard_overview_data_latency_top_routes_by_impact_hint_inner_instance.to_dict()
# create an instance of DashboardOverviewDataLatencyTopRoutesByImpactHintInner from a dict
dashboard_overview_data_latency_top_routes_by_impact_hint_inner_from_dict = DashboardOverviewDataLatencyTopRoutesByImpactHintInner.from_dict(dashboard_overview_data_latency_top_routes_by_impact_hint_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


