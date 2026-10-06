# ProjectEmailSendRequest

Either `template` (with optional `data`) or both `subject` and `html` must be provided. `to` may be a string or array of strings. For named templates, **`data`** should supply values for `{{placeholders}}` (see **Email** tag description for the full list). 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**template** | **str** | Registered template name resolved by the email worker | [optional] 
**to** | [**EmailRequestTo**](EmailRequestTo.md) |  | [optional] 
**data** | **Dict[str, object]** |  | [optional] 
**subject** | **str** |  | [optional] 
**html** | **str** |  | [optional] 
**idempotency_key** | **str** |  | [optional] 
**branding_scope** | **str** | Email layout branding; defaults from project context when omitted | [optional] 

## Example

```python
from mudbase.models.project_email_send_request import ProjectEmailSendRequest

# TODO update the JSON string below
json = "{}"
# create an instance of ProjectEmailSendRequest from a JSON string
project_email_send_request_instance = ProjectEmailSendRequest.from_json(json)
# print the JSON string representation of the object
print(ProjectEmailSendRequest.to_json())

# convert the object into a dict
project_email_send_request_dict = project_email_send_request_instance.to_dict()
# create an instance of ProjectEmailSendRequest from a dict
project_email_send_request_from_dict = ProjectEmailSendRequest.from_dict(project_email_send_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


