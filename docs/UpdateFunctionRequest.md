# UpdateFunctionRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** |  | [optional] 
**description** | **str** |  | [optional] 
**code** | **str** |  | [optional] 
**trigger** | [**FunctionTrigger**](FunctionTrigger.md) |  | [optional] 
**environment** | **object** |  | [optional] 
**is_active** | **bool** |  | [optional] 
**limits** | [**UpdateFunctionRequestLimits**](UpdateFunctionRequestLimits.md) |  | [optional] 
**retry_policy** | [**UpdateFunctionRequestRetryPolicy**](UpdateFunctionRequestRetryPolicy.md) |  | [optional] 
**version_comment** | **str** | Comment for version when code is updated | [optional] 

## Example

```python
from mudbase.models.update_function_request import UpdateFunctionRequest

# TODO update the JSON string below
json = "{}"
# create an instance of UpdateFunctionRequest from a JSON string
update_function_request_instance = UpdateFunctionRequest.from_json(json)
# print the JSON string representation of the object
print(UpdateFunctionRequest.to_json())

# convert the object into a dict
update_function_request_dict = update_function_request_instance.to_dict()
# create an instance of UpdateFunctionRequest from a dict
update_function_request_from_dict = UpdateFunctionRequest.from_dict(update_function_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


