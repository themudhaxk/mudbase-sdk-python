# EmailTemplateCatalogItem

One row from GET /email/templates (full catalog for the project).

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** |  | [optional] 
**is_customized** | **bool** | True if this project has a stored override for this template name. | [optional] 
**effective_source** | **str** | Which layer is used at send time for this name. | [optional] 
**subject_snippet** | **str** |  | [optional] 
**updated_at** | **datetime** |  | [optional] 
**version** | **int** |  | [optional] 

## Example

```python
from mudbase.models.email_template_catalog_item import EmailTemplateCatalogItem

# TODO update the JSON string below
json = "{}"
# create an instance of EmailTemplateCatalogItem from a JSON string
email_template_catalog_item_instance = EmailTemplateCatalogItem.from_json(json)
# print the JSON string representation of the object
print(EmailTemplateCatalogItem.to_json())

# convert the object into a dict
email_template_catalog_item_dict = email_template_catalog_item_instance.to_dict()
# create an instance of EmailTemplateCatalogItem from a dict
email_template_catalog_item_from_dict = EmailTemplateCatalogItem.from_dict(email_template_catalog_item_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


