# GetHistoricalAnalytics200ResponseDataInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**timestamp** | **datetime** |  | [optional] 
**connections** | **int** |  | [optional] 
**events** | **int** |  | [optional] 

## Example

```python
from mudbase.models.get_historical_analytics200_response_data_inner import GetHistoricalAnalytics200ResponseDataInner

# TODO update the JSON string below
json = "{}"
# create an instance of GetHistoricalAnalytics200ResponseDataInner from a JSON string
get_historical_analytics200_response_data_inner_instance = GetHistoricalAnalytics200ResponseDataInner.from_json(json)
# print the JSON string representation of the object
print(GetHistoricalAnalytics200ResponseDataInner.to_json())

# convert the object into a dict
get_historical_analytics200_response_data_inner_dict = get_historical_analytics200_response_data_inner_instance.to_dict()
# create an instance of GetHistoricalAnalytics200ResponseDataInner from a dict
get_historical_analytics200_response_data_inner_from_dict = GetHistoricalAnalytics200ResponseDataInner.from_dict(get_historical_analytics200_response_data_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


