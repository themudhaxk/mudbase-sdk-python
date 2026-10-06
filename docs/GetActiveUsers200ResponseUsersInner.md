# GetActiveUsers200ResponseUsersInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**user_id** | **str** |  | [optional] 
**connected_at** | **datetime** |  | [optional] 
**socket_id** | **str** |  | [optional] 

## Example

```python
from mudbase.models.get_active_users200_response_users_inner import GetActiveUsers200ResponseUsersInner

# TODO update the JSON string below
json = "{}"
# create an instance of GetActiveUsers200ResponseUsersInner from a JSON string
get_active_users200_response_users_inner_instance = GetActiveUsers200ResponseUsersInner.from_json(json)
# print the JSON string representation of the object
print(GetActiveUsers200ResponseUsersInner.to_json())

# convert the object into a dict
get_active_users200_response_users_inner_dict = get_active_users200_response_users_inner_instance.to_dict()
# create an instance of GetActiveUsers200ResponseUsersInner from a dict
get_active_users200_response_users_inner_from_dict = GetActiveUsers200ResponseUsersInner.from_dict(get_active_users200_response_users_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


