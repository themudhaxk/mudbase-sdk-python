# TestIntegration200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**success** | **bool** |  | [optional] 
**data** | **object** |  | [optional] 

## Example

```python
from mudbase.models.test_integration200_response import TestIntegration200Response

# TODO update the JSON string below
json = "{}"
# create an instance of TestIntegration200Response from a JSON string
test_integration200_response_instance = TestIntegration200Response.from_json(json)
# print the JSON string representation of the object
print(TestIntegration200Response.to_json())

# convert the object into a dict
test_integration200_response_dict = test_integration200_response_instance.to_dict()
# create an instance of TestIntegration200Response from a dict
test_integration200_response_from_dict = TestIntegration200Response.from_dict(test_integration200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


