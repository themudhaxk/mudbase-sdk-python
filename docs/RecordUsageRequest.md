# RecordUsageRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**email** | **str** | Customer email | 
**metric** | **str** | Usage metric name (e.g. api_calls, storage_mb) | 
**quantity** | **float** | Quantity to record | 

## Example

```python
from mudbase.models.record_usage_request import RecordUsageRequest

# TODO update the JSON string below
json = "{}"
# create an instance of RecordUsageRequest from a JSON string
record_usage_request_instance = RecordUsageRequest.from_json(json)
# print the JSON string representation of the object
print(RecordUsageRequest.to_json())

# convert the object into a dict
record_usage_request_dict = record_usage_request_instance.to_dict()
# create an instance of RecordUsageRequest from a dict
record_usage_request_from_dict = RecordUsageRequest.from_dict(record_usage_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


