# EmailTemplateResolved

Effective template body (project override, else global, else built-in).

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** |  | [optional] 
**subject** | **str** |  | [optional] 
**html_body** | **str** |  | [optional] 
**text_body** | **str** |  | [optional] 
**variables** | **List[str]** |  | [optional] 
**updated_at** | **datetime** |  | [optional] 
**version** | **int** |  | [optional] 
**is_project_override** | **bool** |  | [optional] 
**effective_source** | **str** |  | [optional] 

## Example

```python
from mudbase.models.email_template_resolved import EmailTemplateResolved

# TODO update the JSON string below
json = "{}"
# create an instance of EmailTemplateResolved from a JSON string
email_template_resolved_instance = EmailTemplateResolved.from_json(json)
# print the JSON string representation of the object
print(EmailTemplateResolved.to_json())

# convert the object into a dict
email_template_resolved_dict = email_template_resolved_instance.to_dict()
# create an instance of EmailTemplateResolved from a dict
email_template_resolved_from_dict = EmailTemplateResolved.from_dict(email_template_resolved_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


