# ProjectSettings

Project-level settings. Toggles for verification and default user status apply to project-based and role-based signup. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**allow_anonymous_auth** | **bool** | Allow anonymous (unauthenticated) users | [optional] [default to True]
**require_email_verification** | **bool** | When true, users who sign up with email do not receive a token until they verify their email; login is blocked until verified. | [optional] [default to True]
**require_phone_verification** | **bool** | When true, users who sign in with phone (e.g. OTP) must have verified their phone before receiving a token. | [optional] [default to False]
**default_user_account_status** | **str** | Default account status for new signups. **active** &#x3D; user can use the app immediately. **pending** &#x3D; user must be approved by an org owner/admin (PATCH org user status to active) before they can perform protected operations.  | [optional] [default to 'active']
**enable_realtime** | **bool** |  | [optional] [default to True]
**enable_storage** | **bool** |  | [optional] [default to True]
**enable_functions** | **bool** |  | [optional] [default to False]

## Example

```python
from mudbase.models.project_settings import ProjectSettings

# TODO update the JSON string below
json = "{}"
# create an instance of ProjectSettings from a JSON string
project_settings_instance = ProjectSettings.from_json(json)
# print the JSON string representation of the object
print(ProjectSettings.to_json())

# convert the object into a dict
project_settings_dict = project_settings_instance.to_dict()
# create an instance of ProjectSettings from a dict
project_settings_from_dict = ProjectSettings.from_dict(project_settings_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


