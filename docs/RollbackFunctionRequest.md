# RollbackFunctionRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**version** | **int** | Version number to rollback to | 

## Example

```python
from mudbase.models.rollback_function_request import RollbackFunctionRequest

# TODO update the JSON string below
json = "{}"
# create an instance of RollbackFunctionRequest from a JSON string
rollback_function_request_instance = RollbackFunctionRequest.from_json(json)
# print the JSON string representation of the object
print(RollbackFunctionRequest.to_json())

# convert the object into a dict
rollback_function_request_dict = rollback_function_request_instance.to_dict()
# create an instance of RollbackFunctionRequest from a dict
rollback_function_request_from_dict = RollbackFunctionRequest.from_dict(rollback_function_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


