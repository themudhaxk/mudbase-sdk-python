# GetProjectFeeDashboard200ResponseDataRecentPayoutsInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** |  | [optional] 
**amount** | **str** |  | [optional] 
**currency** | **str** |  | [optional] 
**status** | **str** |  | [optional] 
**created_at** | **datetime** |  | [optional] 

## Example

```python
from mudbase.models.get_project_fee_dashboard200_response_data_recent_payouts_inner import GetProjectFeeDashboard200ResponseDataRecentPayoutsInner

# TODO update the JSON string below
json = "{}"
# create an instance of GetProjectFeeDashboard200ResponseDataRecentPayoutsInner from a JSON string
get_project_fee_dashboard200_response_data_recent_payouts_inner_instance = GetProjectFeeDashboard200ResponseDataRecentPayoutsInner.from_json(json)
# print the JSON string representation of the object
print(GetProjectFeeDashboard200ResponseDataRecentPayoutsInner.to_json())

# convert the object into a dict
get_project_fee_dashboard200_response_data_recent_payouts_inner_dict = get_project_fee_dashboard200_response_data_recent_payouts_inner_instance.to_dict()
# create an instance of GetProjectFeeDashboard200ResponseDataRecentPayoutsInner from a dict
get_project_fee_dashboard200_response_data_recent_payouts_inner_from_dict = GetProjectFeeDashboard200ResponseDataRecentPayoutsInner.from_dict(get_project_fee_dashboard200_response_data_recent_payouts_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


