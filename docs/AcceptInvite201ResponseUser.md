# AcceptInvite201ResponseUser


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** |  | [optional] 
**email** | **str** |  | [optional] 
**first_name** | **str** |  | [optional] 
**last_name** | **str** |  | [optional] 
**org** | **str** |  | [optional] 
**role** | **str** |  | [optional] 
**email_verified** | **bool** |  | [optional] 

## Example

```python
from mudbase.models.accept_invite201_response_user import AcceptInvite201ResponseUser

# TODO update the JSON string below
json = "{}"
# create an instance of AcceptInvite201ResponseUser from a JSON string
accept_invite201_response_user_instance = AcceptInvite201ResponseUser.from_json(json)
# print the JSON string representation of the object
print(AcceptInvite201ResponseUser.to_json())

# convert the object into a dict
accept_invite201_response_user_dict = accept_invite201_response_user_instance.to_dict()
# create an instance of AcceptInvite201ResponseUser from a dict
accept_invite201_response_user_from_dict = AcceptInvite201ResponseUser.from_dict(accept_invite201_response_user_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


