# MessageStatsResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**success** | **bool** |  | [optional] 
**data** | [**MessageStatsResponseData**](MessageStatsResponseData.md) |  | [optional] 

## Example

```python
from mudbase.models.message_stats_response import MessageStatsResponse

# TODO update the JSON string below
json = "{}"
# create an instance of MessageStatsResponse from a JSON string
message_stats_response_instance = MessageStatsResponse.from_json(json)
# print the JSON string representation of the object
print(MessageStatsResponse.to_json())

# convert the object into a dict
message_stats_response_dict = message_stats_response_instance.to_dict()
# create an instance of MessageStatsResponse from a dict
message_stats_response_from_dict = MessageStatsResponse.from_dict(message_stats_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


