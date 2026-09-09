# CreateAnonymousSession200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**message** | **str** |  | [optional] 
**token** | **str** |  | [optional] 
**refresh_token** | **str** | Refresh token for POST /api/auth/refresh | [optional] 
**expires_in** | **int** |  | [optional] 
**user** | [**CreateAnonymousSession200ResponseUser**](CreateAnonymousSession200ResponseUser.md) |  | [optional] 

## Example

```python
from mudbase.models.create_anonymous_session200_response import CreateAnonymousSession200Response

# TODO update the JSON string below
json = "{}"
# create an instance of CreateAnonymousSession200Response from a JSON string
create_anonymous_session200_response_instance = CreateAnonymousSession200Response.from_json(json)
# print the JSON string representation of the object
print(CreateAnonymousSession200Response.to_json())

# convert the object into a dict
create_anonymous_session200_response_dict = create_anonymous_session200_response_instance.to_dict()
# create an instance of CreateAnonymousSession200Response from a dict
create_anonymous_session200_response_from_dict = CreateAnonymousSession200Response.from_dict(create_anonymous_session200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


