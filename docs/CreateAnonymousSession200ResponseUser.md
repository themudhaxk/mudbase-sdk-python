# CreateAnonymousSession200ResponseUser


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** |  | [optional] 
**email** | **str** |  | [optional] 
**first_name** | **str** |  | [optional] 
**last_name** | **str** |  | [optional] 
**role** | **str** |  | [optional] 
**is_anonymous** | **bool** |  | [optional] 

## Example

```python
from mudbase.models.create_anonymous_session200_response_user import CreateAnonymousSession200ResponseUser

# TODO update the JSON string below
json = "{}"
# create an instance of CreateAnonymousSession200ResponseUser from a JSON string
create_anonymous_session200_response_user_instance = CreateAnonymousSession200ResponseUser.from_json(json)
# print the JSON string representation of the object
print(CreateAnonymousSession200ResponseUser.to_json())

# convert the object into a dict
create_anonymous_session200_response_user_dict = create_anonymous_session200_response_user_instance.to_dict()
# create an instance of CreateAnonymousSession200ResponseUser from a dict
create_anonymous_session200_response_user_from_dict = CreateAnonymousSession200ResponseUser.from_dict(create_anonymous_session200_response_user_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


