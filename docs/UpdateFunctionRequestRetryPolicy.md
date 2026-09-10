# UpdateFunctionRequestRetryPolicy


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**enabled** | **bool** |  | [optional] 
**max_retries** | **int** |  | [optional] 
**backoff_ms** | **int** |  | [optional] 

## Example

```python
from mudbase.models.update_function_request_retry_policy import UpdateFunctionRequestRetryPolicy

# TODO update the JSON string below
json = "{}"
# create an instance of UpdateFunctionRequestRetryPolicy from a JSON string
update_function_request_retry_policy_instance = UpdateFunctionRequestRetryPolicy.from_json(json)
# print the JSON string representation of the object
print(UpdateFunctionRequestRetryPolicy.to_json())

# convert the object into a dict
update_function_request_retry_policy_dict = update_function_request_retry_policy_instance.to_dict()
# create an instance of UpdateFunctionRequestRetryPolicy from a dict
update_function_request_retry_policy_from_dict = UpdateFunctionRequestRetryPolicy.from_dict(update_function_request_retry_policy_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


