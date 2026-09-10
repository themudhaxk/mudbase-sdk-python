# ExecuteIntegrationRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**endpoint** | **str** |  | 
**method** | **str** |  | 
**params** | **object** |  | [optional] 
**body** | **object** |  | [optional] 

## Example

```python
from mudbase.models.execute_integration_request import ExecuteIntegrationRequest

# TODO update the JSON string below
json = "{}"
# create an instance of ExecuteIntegrationRequest from a JSON string
execute_integration_request_instance = ExecuteIntegrationRequest.from_json(json)
# print the JSON string representation of the object
print(ExecuteIntegrationRequest.to_json())

# convert the object into a dict
execute_integration_request_dict = execute_integration_request_instance.to_dict()
# create an instance of ExecuteIntegrationRequest from a dict
execute_integration_request_from_dict = ExecuteIntegrationRequest.from_dict(execute_integration_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


