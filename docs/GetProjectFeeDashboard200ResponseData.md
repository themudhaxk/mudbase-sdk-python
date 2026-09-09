# GetProjectFeeDashboard200ResponseData


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**fee_settings** | **object** |  | [optional] 
**balances** | [**List[GetProjectFeeDashboard200ResponseDataBalancesInner]**](GetProjectFeeDashboard200ResponseDataBalancesInner.md) |  | [optional] 
**recent_payouts** | [**List[GetProjectFeeDashboard200ResponseDataRecentPayoutsInner]**](GetProjectFeeDashboard200ResponseDataRecentPayoutsInner.md) |  | [optional] 
**total_earned** | **float** |  | [optional] 

## Example

```python
from mudbase.models.get_project_fee_dashboard200_response_data import GetProjectFeeDashboard200ResponseData

# TODO update the JSON string below
json = "{}"
# create an instance of GetProjectFeeDashboard200ResponseData from a JSON string
get_project_fee_dashboard200_response_data_instance = GetProjectFeeDashboard200ResponseData.from_json(json)
# print the JSON string representation of the object
print(GetProjectFeeDashboard200ResponseData.to_json())

# convert the object into a dict
get_project_fee_dashboard200_response_data_dict = get_project_fee_dashboard200_response_data_instance.to_dict()
# create an instance of GetProjectFeeDashboard200ResponseData from a dict
get_project_fee_dashboard200_response_data_from_dict = GetProjectFeeDashboard200ResponseData.from_dict(get_project_fee_dashboard200_response_data_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


