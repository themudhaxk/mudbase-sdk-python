# ProjectSmtpPatchRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**enabled** | **bool** |  | [optional] 
**host** | **str** |  | [optional] 
**port** | **int** |  | [optional] 
**secure** | **bool** |  | [optional] 
**auth_user** | **str** |  | [optional] 
**auth_pass** | **str** | SMTP password; stored encrypted, never returned on GET | [optional] 
**from_name** | **str** |  | [optional] 
**from_email** | **str** |  | [optional] 
**domain_verified_at** | **datetime** |  | [optional] 

## Example

```python
from mudbase.models.project_smtp_patch_request import ProjectSmtpPatchRequest

# TODO update the JSON string below
json = "{}"
# create an instance of ProjectSmtpPatchRequest from a JSON string
project_smtp_patch_request_instance = ProjectSmtpPatchRequest.from_json(json)
# print the JSON string representation of the object
print(ProjectSmtpPatchRequest.to_json())

# convert the object into a dict
project_smtp_patch_request_dict = project_smtp_patch_request_instance.to_dict()
# create an instance of ProjectSmtpPatchRequest from a dict
project_smtp_patch_request_from_dict = ProjectSmtpPatchRequest.from_dict(project_smtp_patch_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


