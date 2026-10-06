# UpdateUserAccountStatusRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_status** | **str** | active &#x3D; full access; suspended &#x3D; blocked from using the app | 

## Example

```python
from mudbase.models.update_user_account_status_request import UpdateUserAccountStatusRequest

# TODO update the JSON string below
json = "{}"
# create an instance of UpdateUserAccountStatusRequest from a JSON string
update_user_account_status_request_instance = UpdateUserAccountStatusRequest.from_json(json)
# print the JSON string representation of the object
print(UpdateUserAccountStatusRequest.to_json())

# convert the object into a dict
update_user_account_status_request_dict = update_user_account_status_request_instance.to_dict()
# create an instance of UpdateUserAccountStatusRequest from a dict
update_user_account_status_request_from_dict = UpdateUserAccountStatusRequest.from_dict(update_user_account_status_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


