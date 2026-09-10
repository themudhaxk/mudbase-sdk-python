# TestIntegrationRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**endpoint** | **str** |  | [optional] 
**method** | **str** |  | [optional] 
**params** | **object** |  | [optional] 

## Example

```python
from mudbase.models.test_integration_request import TestIntegrationRequest

# TODO update the JSON string below
json = "{}"
# create an instance of TestIntegrationRequest from a JSON string
test_integration_request_instance = TestIntegrationRequest.from_json(json)
# print the JSON string representation of the object
print(TestIntegrationRequest.to_json())

# convert the object into a dict
test_integration_request_dict = test_integration_request_instance.to_dict()
# create an instance of TestIntegrationRequest from a dict
test_integration_request_from_dict = TestIntegrationRequest.from_dict(test_integration_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


