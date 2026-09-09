# DashboardActivityItem


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** |  | [optional] 
**at** | **datetime** |  | [optional] 
**action** | **str** |  | [optional] 
**title** | **str** |  | [optional] 
**detail** | **str** |  | [optional] 
**actor_email** | **str** |  | [optional] 

## Example

```python
from mudbase.models.dashboard_activity_item import DashboardActivityItem

# TODO update the JSON string below
json = "{}"
# create an instance of DashboardActivityItem from a JSON string
dashboard_activity_item_instance = DashboardActivityItem.from_json(json)
# print the JSON string representation of the object
print(DashboardActivityItem.to_json())

# convert the object into a dict
dashboard_activity_item_dict = dashboard_activity_item_instance.to_dict()
# create an instance of DashboardActivityItem from a dict
dashboard_activity_item_from_dict = DashboardActivityItem.from_dict(dashboard_activity_item_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


