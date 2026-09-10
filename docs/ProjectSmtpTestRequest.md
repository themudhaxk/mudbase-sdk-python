# ProjectSmtpTestRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**to** | **str** | Recipient for verification and test message | 
**use_saved** | **bool** | When true, use saved SMTP config; otherwise supply host/auth fields below | [optional] [default to True]
**host** | **str** |  | [optional] 
**port** | **int** |  | [optional] 
**secure** | **bool** |  | [optional] 
**auth_user** | **str** |  | [optional] 
**auth_pass** | **str** |  | [optional] 
**from_email** | **str** |  | [optional] 
**from_name** | **str** |  | [optional] 

## Example

```python
from mudbase.models.project_smtp_test_request import ProjectSmtpTestRequest

# TODO update the JSON string below
json = "{}"
# create an instance of ProjectSmtpTestRequest from a JSON string
project_smtp_test_request_instance = ProjectSmtpTestRequest.from_json(json)
# print the JSON string representation of the object
print(ProjectSmtpTestRequest.to_json())

# convert the object into a dict
project_smtp_test_request_dict = project_smtp_test_request_instance.to_dict()
# create an instance of ProjectSmtpTestRequest from a dict
project_smtp_test_request_from_dict = ProjectSmtpTestRequest.from_dict(project_smtp_test_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


