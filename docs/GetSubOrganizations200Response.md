# GetSubOrganizations200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**suborgs** | [**List[Organization]**](Organization.md) |  | [optional] 
**total** | **int** |  | [optional] 

## Example

```python
from mudbase.models.get_sub_organizations200_response import GetSubOrganizations200Response

# TODO update the JSON string below
json = "{}"
# create an instance of GetSubOrganizations200Response from a JSON string
get_sub_organizations200_response_instance = GetSubOrganizations200Response.from_json(json)
# print the JSON string representation of the object
print(GetSubOrganizations200Response.to_json())

# convert the object into a dict
get_sub_organizations200_response_dict = get_sub_organizations200_response_instance.to_dict()
# create an instance of GetSubOrganizations200Response from a dict
get_sub_organizations200_response_from_dict = GetSubOrganizations200Response.from_dict(get_sub_organizations200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


