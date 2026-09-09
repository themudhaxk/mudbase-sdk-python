# GetOrganizationMembers200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**members** | [**List[User]**](User.md) |  | [optional] 
**total** | **int** |  | [optional] 

## Example

```python
from mudbase.models.get_organization_members200_response import GetOrganizationMembers200Response

# TODO update the JSON string below
json = "{}"
# create an instance of GetOrganizationMembers200Response from a JSON string
get_organization_members200_response_instance = GetOrganizationMembers200Response.from_json(json)
# print the JSON string representation of the object
print(GetOrganizationMembers200Response.to_json())

# convert the object into a dict
get_organization_members200_response_dict = get_organization_members200_response_instance.to_dict()
# create an instance of GetOrganizationMembers200Response from a dict
get_organization_members200_response_from_dict = GetOrganizationMembers200Response.from_dict(get_organization_members200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


