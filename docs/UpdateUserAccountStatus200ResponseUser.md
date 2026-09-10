# UpdateUserAccountStatus200ResponseUser


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** |  | [optional] 
**email** | **str** |  | [optional] 
**first_name** | **str** |  | [optional] 
**last_name** | **str** |  | [optional] 
**account_status** | **str** |  | [optional] 
**is_active** | **bool** |  | [optional] 

## Example

```python
from mudbase.models.update_user_account_status200_response_user import UpdateUserAccountStatus200ResponseUser

# TODO update the JSON string below
json = "{}"
# create an instance of UpdateUserAccountStatus200ResponseUser from a JSON string
update_user_account_status200_response_user_instance = UpdateUserAccountStatus200ResponseUser.from_json(json)
# print the JSON string representation of the object
print(UpdateUserAccountStatus200ResponseUser.to_json())

# convert the object into a dict
update_user_account_status200_response_user_dict = update_user_account_status200_response_user_instance.to_dict()
# create an instance of UpdateUserAccountStatus200ResponseUser from a dict
update_user_account_status200_response_user_from_dict = UpdateUserAccountStatus200ResponseUser.from_dict(update_user_account_status200_response_user_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


