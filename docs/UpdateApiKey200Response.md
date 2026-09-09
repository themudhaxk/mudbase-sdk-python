# UpdateApiKey200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**message** | **str** |  | [optional] 
**api_key** | [**ApiKey**](ApiKey.md) |  | [optional] 

## Example

```python
from mudbase.models.update_api_key200_response import UpdateApiKey200Response

# TODO update the JSON string below
json = "{}"
# create an instance of UpdateApiKey200Response from a JSON string
update_api_key200_response_instance = UpdateApiKey200Response.from_json(json)
# print the JSON string representation of the object
print(UpdateApiKey200Response.to_json())

# convert the object into a dict
update_api_key200_response_dict = update_api_key200_response_instance.to_dict()
# create an instance of UpdateApiKey200Response from a dict
update_api_key200_response_from_dict = UpdateApiKey200Response.from_dict(update_api_key200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


