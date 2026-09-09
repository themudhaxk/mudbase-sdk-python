# GetOrganizationUsers200ResponseUsersInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** |  | [optional] 
**first_name** | **str** |  | [optional] 
**last_name** | **str** |  | [optional] 
**email** | **str** |  | [optional] 
**avatar** | **str** |  | [optional] 
**email_verified** | **bool** |  | [optional] 
**role** | **str** |  | [optional] 
**custom_role** | **str** |  | [optional] 
**phone** | **str** |  | [optional] 
**phone_verified** | **bool** |  | [optional] 
**last_login** | **datetime** |  | [optional] 
**is_active** | **bool** |  | [optional] 
**account_status** | **str** |  | [optional] 
**is_anonymous** | **bool** |  | [optional] 
**created_at** | **datetime** |  | [optional] 
**project** | [**GetOrganizationUsers200ResponseUsersInnerProject**](GetOrganizationUsers200ResponseUsersInnerProject.md) |  | [optional] 

## Example

```python
from mudbase.models.get_organization_users200_response_users_inner import GetOrganizationUsers200ResponseUsersInner

# TODO update the JSON string below
json = "{}"
# create an instance of GetOrganizationUsers200ResponseUsersInner from a JSON string
get_organization_users200_response_users_inner_instance = GetOrganizationUsers200ResponseUsersInner.from_json(json)
# print the JSON string representation of the object
print(GetOrganizationUsers200ResponseUsersInner.to_json())

# convert the object into a dict
get_organization_users200_response_users_inner_dict = get_organization_users200_response_users_inner_instance.to_dict()
# create an instance of GetOrganizationUsers200ResponseUsersInner from a dict
get_organization_users200_response_users_inner_from_dict = GetOrganizationUsers200ResponseUsersInner.from_dict(get_organization_users200_response_users_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


