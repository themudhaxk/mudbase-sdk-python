# AcceptInvite201Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**message** | **str** |  | [optional] 
**token** | **str** | JWT for the new user session | [optional] 
**user** | [**AcceptInvite201ResponseUser**](AcceptInvite201ResponseUser.md) |  | [optional] 

## Example

```python
from mudbase.models.accept_invite201_response import AcceptInvite201Response

# TODO update the JSON string below
json = "{}"
# create an instance of AcceptInvite201Response from a JSON string
accept_invite201_response_instance = AcceptInvite201Response.from_json(json)
# print the JSON string representation of the object
print(AcceptInvite201Response.to_json())

# convert the object into a dict
accept_invite201_response_dict = accept_invite201_response_instance.to_dict()
# create an instance of AcceptInvite201Response from a dict
accept_invite201_response_from_dict = AcceptInvite201Response.from_dict(accept_invite201_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


