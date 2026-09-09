# GetOrganizationUsers200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**users** | [**List[GetOrganizationUsers200ResponseUsersInner]**](GetOrganizationUsers200ResponseUsersInner.md) |  | [optional] 
**total** | **int** |  | [optional] 

## Example

```python
from mudbase.models.get_organization_users200_response import GetOrganizationUsers200Response

# TODO update the JSON string below
json = "{}"
# create an instance of GetOrganizationUsers200Response from a JSON string
get_organization_users200_response_instance = GetOrganizationUsers200Response.from_json(json)
# print the JSON string representation of the object
print(GetOrganizationUsers200Response.to_json())

# convert the object into a dict
get_organization_users200_response_dict = get_organization_users200_response_instance.to_dict()
# create an instance of GetOrganizationUsers200Response from a dict
get_organization_users200_response_from_dict = GetOrganizationUsers200Response.from_dict(get_organization_users200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


