# CreateFromTemplateRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**template_id** | **str** |  | 
**credentials** | **object** |  | 
**name** | **str** |  | [optional] 

## Example

```python
from mudbase.models.create_from_template_request import CreateFromTemplateRequest

# TODO update the JSON string below
json = "{}"
# create an instance of CreateFromTemplateRequest from a JSON string
create_from_template_request_instance = CreateFromTemplateRequest.from_json(json)
# print the JSON string representation of the object
print(CreateFromTemplateRequest.to_json())

# convert the object into a dict
create_from_template_request_dict = create_from_template_request_instance.to_dict()
# create an instance of CreateFromTemplateRequest from a dict
create_from_template_request_from_dict = CreateFromTemplateRequest.from_dict(create_from_template_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


