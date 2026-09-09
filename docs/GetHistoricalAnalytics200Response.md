# GetHistoricalAnalytics200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**project_id** | **str** |  | [optional] 
**period** | **str** |  | [optional] 
**data** | [**List[GetHistoricalAnalytics200ResponseDataInner]**](GetHistoricalAnalytics200ResponseDataInner.md) |  | [optional] 
**generated_at** | **datetime** |  | [optional] 

## Example

```python
from mudbase.models.get_historical_analytics200_response import GetHistoricalAnalytics200Response

# TODO update the JSON string below
json = "{}"
# create an instance of GetHistoricalAnalytics200Response from a JSON string
get_historical_analytics200_response_instance = GetHistoricalAnalytics200Response.from_json(json)
# print the JSON string representation of the object
print(GetHistoricalAnalytics200Response.to_json())

# convert the object into a dict
get_historical_analytics200_response_dict = get_historical_analytics200_response_instance.to_dict()
# create an instance of GetHistoricalAnalytics200Response from a dict
get_historical_analytics200_response_from_dict = GetHistoricalAnalytics200Response.from_dict(get_historical_analytics200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


