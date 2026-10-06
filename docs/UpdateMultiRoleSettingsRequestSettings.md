# UpdateMultiRoleSettingsRequestSettings

Feature toggles for signup behavior (not per-role approval flags).

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**allow_multiple_roles** | **bool** | Whether an end user may hold multiple app roles. | [optional] 
**require_role_selection** | **bool** | If true, signup must pick a role; if false and &#x60;autoAssignDefault&#x60; is true, &#x60;defaultRole&#x60; is used when omitted. | [optional] 
**auto_assign_default** | **bool** | When true, assigns &#x60;defaultRole&#x60; when the client does not specify a role at signup. | [optional] 
**data_owner_field** | **str** | Default document field for dataScope &#x60;own&#x60; (e.g. createdBy, userId). | [optional] [default to 'createdBy']

## Example

```python
from mudbase.models.update_multi_role_settings_request_settings import UpdateMultiRoleSettingsRequestSettings

# TODO update the JSON string below
json = "{}"
# create an instance of UpdateMultiRoleSettingsRequestSettings from a JSON string
update_multi_role_settings_request_settings_instance = UpdateMultiRoleSettingsRequestSettings.from_json(json)
# print the JSON string representation of the object
print(UpdateMultiRoleSettingsRequestSettings.to_json())

# convert the object into a dict
update_multi_role_settings_request_settings_dict = update_multi_role_settings_request_settings_instance.to_dict()
# create an instance of UpdateMultiRoleSettingsRequestSettings from a dict
update_multi_role_settings_request_settings_from_dict = UpdateMultiRoleSettingsRequestSettings.from_dict(update_multi_role_settings_request_settings_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


