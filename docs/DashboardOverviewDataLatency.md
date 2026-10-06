# DashboardOverviewDataLatency

Per-project weighted mean latency from UsageStat for routes in openapi-docs.yaml (customer/project API only).

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**scope** | **str** |  | [optional] 
**avg_ms_today** | **int** |  | [optional] 
**avg_ms7d** | **int** |  | [optional] 
**latency_samples_today** | **int** | Count of openapi-docs–scoped latency samples for this project (UTC today) | [optional] 
**latency_needs_traffic** | **bool** |  | [optional] 
**interpretation** | **str** | Why mean can differ from typical latency; points to latency-insights | [optional] 
**instance_rollup** | [**DashboardOverviewDataLatencyInstanceRollup**](DashboardOverviewDataLatencyInstanceRollup.md) |  | [optional] 
**top_routes_by_impact_hint** | [**List[DashboardOverviewDataLatencyTopRoutesByImpactHintInner]**](DashboardOverviewDataLatencyTopRoutesByImpactHintInner.md) | Top route templates by impact score on this instance (debugging hint) | [optional] 

## Example

```python
from mudbase.models.dashboard_overview_data_latency import DashboardOverviewDataLatency

# TODO update the JSON string below
json = "{}"
# create an instance of DashboardOverviewDataLatency from a JSON string
dashboard_overview_data_latency_instance = DashboardOverviewDataLatency.from_json(json)
# print the JSON string representation of the object
print(DashboardOverviewDataLatency.to_json())

# convert the object into a dict
dashboard_overview_data_latency_dict = dashboard_overview_data_latency_instance.to_dict()
# create an instance of DashboardOverviewDataLatency from a dict
dashboard_overview_data_latency_from_dict = DashboardOverviewDataLatency.from_dict(dashboard_overview_data_latency_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


