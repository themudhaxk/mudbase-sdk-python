# GetLocalSession200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**user** | **object** |  | [optional] 
**authenticated** | **bool** |  | [optional] 

## Example

```python
from mudbase.models.get_local_session200_response import GetLocalSession200Response

# TODO update the JSON string below
json = "{}"
# create an instance of GetLocalSession200Response from a JSON string
get_local_session200_response_instance = GetLocalSession200Response.from_json(json)
# print the JSON string representation of the object
print(GetLocalSession200Response.to_json())

# convert the object into a dict
get_local_session200_response_dict = get_local_session200_response_instance.to_dict()
# create an instance of GetLocalSession200Response from a dict
get_local_session200_response_from_dict = GetLocalSession200Response.from_dict(get_local_session200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


