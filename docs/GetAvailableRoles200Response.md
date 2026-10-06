# GetAvailableRoles200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**success** | **bool** |  | [optional] 
**data** | [**List[GetAvailableRoles200ResponseDataInner]**](GetAvailableRoles200ResponseDataInner.md) |  | [optional] 

## Example

```python
from mudbase.models.get_available_roles200_response import GetAvailableRoles200Response

# TODO update the JSON string below
json = "{}"
# create an instance of GetAvailableRoles200Response from a JSON string
get_available_roles200_response_instance = GetAvailableRoles200Response.from_json(json)
# print the JSON string representation of the object
print(GetAvailableRoles200Response.to_json())

# convert the object into a dict
get_available_roles200_response_dict = get_available_roles200_response_instance.to_dict()
# create an instance of GetAvailableRoles200Response from a dict
get_available_roles200_response_from_dict = GetAvailableRoles200Response.from_dict(get_available_roles200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


