# RefreshToken200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**message** | **str** |  | [optional] 
**token** | **str** | New JWT access token | [optional] 
**refresh_token** | **str** | New refresh token (store and use for next refresh) | [optional] 
**expires_in** | **int** | Access token TTL in seconds | [optional] 

## Example

```python
from mudbase.models.refresh_token200_response import RefreshToken200Response

# TODO update the JSON string below
json = "{}"
# create an instance of RefreshToken200Response from a JSON string
refresh_token200_response_instance = RefreshToken200Response.from_json(json)
# print the JSON string representation of the object
print(RefreshToken200Response.to_json())

# convert the object into a dict
refresh_token200_response_dict = refresh_token200_response_instance.to_dict()
# create an instance of RefreshToken200Response from a dict
refresh_token200_response_from_dict = RefreshToken200Response.from_dict(refresh_token200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


