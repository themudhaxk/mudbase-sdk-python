# RegenerateApiKey200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**message** | **str** |  | [optional] 
**secret** | **str** |  | [optional] 

## Example

```python
from mudbase.models.regenerate_api_key200_response import RegenerateApiKey200Response

# TODO update the JSON string below
json = "{}"
# create an instance of RegenerateApiKey200Response from a JSON string
regenerate_api_key200_response_instance = RegenerateApiKey200Response.from_json(json)
# print the JSON string representation of the object
print(RegenerateApiKey200Response.to_json())

# convert the object into a dict
regenerate_api_key200_response_dict = regenerate_api_key200_response_instance.to_dict()
# create an instance of RegenerateApiKey200Response from a dict
regenerate_api_key200_response_from_dict = RegenerateApiKey200Response.from_dict(regenerate_api_key200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


