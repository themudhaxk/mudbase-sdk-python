# ApiMeBootstrapGet200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**user** | **object** |  | [optional] 
**organizations** | **List[object]** |  | [optional] 
**default_org** | **object** |  | [optional] 
**projects** | **List[object]** |  | [optional] 

## Example

```python
from mudbase.models.api_me_bootstrap_get200_response import ApiMeBootstrapGet200Response

# TODO update the JSON string below
json = "{}"
# create an instance of ApiMeBootstrapGet200Response from a JSON string
api_me_bootstrap_get200_response_instance = ApiMeBootstrapGet200Response.from_json(json)
# print the JSON string representation of the object
print(ApiMeBootstrapGet200Response.to_json())

# convert the object into a dict
api_me_bootstrap_get200_response_dict = api_me_bootstrap_get200_response_instance.to_dict()
# create an instance of ApiMeBootstrapGet200Response from a dict
api_me_bootstrap_get200_response_from_dict = ApiMeBootstrapGet200Response.from_dict(api_me_bootstrap_get200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


