# UnlinkOAuthProvider200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**message** | **str** |  | [optional] 
**provider** | **str** |  | [optional] 

## Example

```python
from mudbase.models.unlink_o_auth_provider200_response import UnlinkOAuthProvider200Response

# TODO update the JSON string below
json = "{}"
# create an instance of UnlinkOAuthProvider200Response from a JSON string
unlink_o_auth_provider200_response_instance = UnlinkOAuthProvider200Response.from_json(json)
# print the JSON string representation of the object
print(UnlinkOAuthProvider200Response.to_json())

# convert the object into a dict
unlink_o_auth_provider200_response_dict = unlink_o_auth_provider200_response_instance.to_dict()
# create an instance of UnlinkOAuthProvider200Response from a dict
unlink_o_auth_provider200_response_from_dict = UnlinkOAuthProvider200Response.from_dict(unlink_o_auth_provider200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


