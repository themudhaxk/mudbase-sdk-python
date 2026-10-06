# ProjectSmtpSettingsPublic


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**enabled** | **bool** |  | [optional] 
**host** | **str** |  | [optional] 
**port** | **int** |  | [optional] 
**secure** | **bool** |  | [optional] 
**auth_user** | **str** |  | [optional] 
**has_password** | **bool** |  | [optional] 
**from_name** | **str** |  | [optional] 
**from_email** | **str** |  | [optional] 
**domain_verified_at** | **datetime** |  | [optional] 

## Example

```python
from mudbase.models.project_smtp_settings_public import ProjectSmtpSettingsPublic

# TODO update the JSON string below
json = "{}"
# create an instance of ProjectSmtpSettingsPublic from a JSON string
project_smtp_settings_public_instance = ProjectSmtpSettingsPublic.from_json(json)
# print the JSON string representation of the object
print(ProjectSmtpSettingsPublic.to_json())

# convert the object into a dict
project_smtp_settings_public_dict = project_smtp_settings_public_instance.to_dict()
# create an instance of ProjectSmtpSettingsPublic from a dict
project_smtp_settings_public_from_dict = ProjectSmtpSettingsPublic.from_dict(project_smtp_settings_public_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


