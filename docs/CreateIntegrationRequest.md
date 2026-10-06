# CreateIntegrationRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** |  | 
**provider** | **str** |  | 
**config** | **object** |  | 
**credentials** | **object** |  | [optional] 

## Example

```python
from mudbase.models.create_integration_request import CreateIntegrationRequest

# TODO update the JSON string below
json = "{}"
# create an instance of CreateIntegrationRequest from a JSON string
create_integration_request_instance = CreateIntegrationRequest.from_json(json)
# print the JSON string representation of the object
print(CreateIntegrationRequest.to_json())

# convert the object into a dict
create_integration_request_dict = create_integration_request_instance.to_dict()
# create an instance of CreateIntegrationRequest from a dict
create_integration_request_from_dict = CreateIntegrationRequest.from_dict(create_integration_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


