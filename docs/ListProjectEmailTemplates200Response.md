# ListProjectEmailTemplates200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**success** | **bool** |  | [optional] 
**data** | [**List[EmailTemplateCatalogItem]**](EmailTemplateCatalogItem.md) |  | [optional] 

## Example

```python
from mudbase.models.list_project_email_templates200_response import ListProjectEmailTemplates200Response

# TODO update the JSON string below
json = "{}"
# create an instance of ListProjectEmailTemplates200Response from a JSON string
list_project_email_templates200_response_instance = ListProjectEmailTemplates200Response.from_json(json)
# print the JSON string representation of the object
print(ListProjectEmailTemplates200Response.to_json())

# convert the object into a dict
list_project_email_templates200_response_dict = list_project_email_templates200_response_instance.to_dict()
# create an instance of ListProjectEmailTemplates200Response from a dict
list_project_email_templates200_response_from_dict = ListProjectEmailTemplates200Response.from_dict(list_project_email_templates200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


