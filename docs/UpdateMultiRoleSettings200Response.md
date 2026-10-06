# UpdateMultiRoleSettings200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**success** | **bool** |  | [optional] 
**message** | **str** |  | [optional] 
**data** | **object** | Same shape as GET &#x60;/multi-role&#x60; — &#x60;isEnabled&#x60;, &#x60;defaultRole&#x60;, &#x60;settings&#x60;, and &#x60;roles&#x60; (no raw MultiRoleFeature document). | [optional] 

## Example

```python
from mudbase.models.update_multi_role_settings200_response import UpdateMultiRoleSettings200Response

# TODO update the JSON string below
json = "{}"
# create an instance of UpdateMultiRoleSettings200Response from a JSON string
update_multi_role_settings200_response_instance = UpdateMultiRoleSettings200Response.from_json(json)
# print the JSON string representation of the object
print(UpdateMultiRoleSettings200Response.to_json())

# convert the object into a dict
update_multi_role_settings200_response_dict = update_multi_role_settings200_response_instance.to_dict()
# create an instance of UpdateMultiRoleSettings200Response from a dict
update_multi_role_settings200_response_from_dict = UpdateMultiRoleSettings200Response.from_dict(update_multi_role_settings200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


