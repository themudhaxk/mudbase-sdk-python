# GetIntegration200ResponseIntegration


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** |  | [optional] 
**name** | **str** |  | [optional] 
**provider** | **str** |  | [optional] 
**project** | **str** |  | [optional] 
**status** | **str** |  | [optional] 
**config** | **object** |  | [optional] 
**created_at** | **datetime** |  | [optional] 

## Example

```python
from mudbase.models.get_integration200_response_integration import GetIntegration200ResponseIntegration

# TODO update the JSON string below
json = "{}"
# create an instance of GetIntegration200ResponseIntegration from a JSON string
get_integration200_response_integration_instance = GetIntegration200ResponseIntegration.from_json(json)
# print the JSON string representation of the object
print(GetIntegration200ResponseIntegration.to_json())

# convert the object into a dict
get_integration200_response_integration_dict = get_integration200_response_integration_instance.to_dict()
# create an instance of GetIntegration200ResponseIntegration from a dict
get_integration200_response_integration_from_dict = GetIntegration200ResponseIntegration.from_dict(get_integration200_response_integration_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


