# GetEventThroughput200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**window_ms** | **int** |  | [optional] 
**total_events** | **int** |  | [optional] 
**events_per_second** | **float** |  | [optional] 
**by_type** | **Dict[str, int]** |  | [optional] 
**timestamp** | **datetime** |  | [optional] 

## Example

```python
from mudbase.models.get_event_throughput200_response import GetEventThroughput200Response

# TODO update the JSON string below
json = "{}"
# create an instance of GetEventThroughput200Response from a JSON string
get_event_throughput200_response_instance = GetEventThroughput200Response.from_json(json)
# print the JSON string representation of the object
print(GetEventThroughput200Response.to_json())

# convert the object into a dict
get_event_throughput200_response_dict = get_event_throughput200_response_instance.to_dict()
# create an instance of GetEventThroughput200Response from a dict
get_event_throughput200_response_from_dict = GetEventThroughput200Response.from_dict(get_event_throughput200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


