# GetFeeBreakdown200ResponseData


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**amount** | **float** |  | [optional] 
**currency** | **str** |  | [optional] 
**org_receives** | **float** |  | [optional] 
**platform_percent** | **float** |  | [optional] 
**platform_fixed** | **float** |  | [optional] 
**processing_fee** | **float** |  | [optional] 

## Example

```python
from mudbase.models.get_fee_breakdown200_response_data import GetFeeBreakdown200ResponseData

# TODO update the JSON string below
json = "{}"
# create an instance of GetFeeBreakdown200ResponseData from a JSON string
get_fee_breakdown200_response_data_instance = GetFeeBreakdown200ResponseData.from_json(json)
# print the JSON string representation of the object
print(GetFeeBreakdown200ResponseData.to_json())

# convert the object into a dict
get_fee_breakdown200_response_data_dict = get_fee_breakdown200_response_data_instance.to_dict()
# create an instance of GetFeeBreakdown200ResponseData from a dict
get_fee_breakdown200_response_data_from_dict = GetFeeBreakdown200ResponseData.from_dict(get_fee_breakdown200_response_data_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


