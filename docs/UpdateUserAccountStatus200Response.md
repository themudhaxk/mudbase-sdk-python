# UpdateUserAccountStatus200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**message** | **str** |  | [optional] 
**user** | [**UpdateUserAccountStatus200ResponseUser**](UpdateUserAccountStatus200ResponseUser.md) |  | [optional] 

## Example

```python
from mudbase.models.update_user_account_status200_response import UpdateUserAccountStatus200Response

# TODO update the JSON string below
json = "{}"
# create an instance of UpdateUserAccountStatus200Response from a JSON string
update_user_account_status200_response_instance = UpdateUserAccountStatus200Response.from_json(json)
# print the JSON string representation of the object
print(UpdateUserAccountStatus200Response.to_json())

# convert the object into a dict
update_user_account_status200_response_dict = update_user_account_status200_response_instance.to_dict()
# create an instance of UpdateUserAccountStatus200Response from a dict
update_user_account_status200_response_from_dict = UpdateUserAccountStatus200Response.from_dict(update_user_account_status200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


