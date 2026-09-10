# UpdateMultiRoleSettingsRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**is_enabled** | **bool** |  | [optional] 
**default_role** | **str** |  | [optional] 
**settings** | [**UpdateMultiRoleSettingsRequestSettings**](UpdateMultiRoleSettingsRequestSettings.md) |  | [optional] 

## Example

```python
from mudbase.models.update_multi_role_settings_request import UpdateMultiRoleSettingsRequest

# TODO update the JSON string below
json = "{}"
# create an instance of UpdateMultiRoleSettingsRequest from a JSON string
update_multi_role_settings_request_instance = UpdateMultiRoleSettingsRequest.from_json(json)
# print the JSON string representation of the object
print(UpdateMultiRoleSettingsRequest.to_json())

# convert the object into a dict
update_multi_role_settings_request_dict = update_multi_role_settings_request_instance.to_dict()
# create an instance of UpdateMultiRoleSettingsRequest from a dict
update_multi_role_settings_request_from_dict = UpdateMultiRoleSettingsRequest.from_dict(update_multi_role_settings_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


