# UpsertProjectEmailTemplateRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**subject** | **str** |  | 
**html_body** | **str** |  | 
**text_body** | **str** |  | [optional] 
**variables** | **List[str]** |  | [optional] 

## Example

```python
from mudbase.models.upsert_project_email_template_request import UpsertProjectEmailTemplateRequest

# TODO update the JSON string below
json = "{}"
# create an instance of UpsertProjectEmailTemplateRequest from a JSON string
upsert_project_email_template_request_instance = UpsertProjectEmailTemplateRequest.from_json(json)
# print the JSON string representation of the object
print(UpsertProjectEmailTemplateRequest.to_json())

# convert the object into a dict
upsert_project_email_template_request_dict = upsert_project_email_template_request_instance.to_dict()
# create an instance of UpsertProjectEmailTemplateRequest from a dict
upsert_project_email_template_request_from_dict = UpsertProjectEmailTemplateRequest.from_dict(upsert_project_email_template_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


