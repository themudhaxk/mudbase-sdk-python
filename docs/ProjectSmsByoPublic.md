# ProjectSmsByoPublic


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**enabled** | **bool** |  | [optional] 
**provider** | **str** |  | [optional] 
**default_from** | **str** |  | [optional] 
**has_credentials** | **bool** |  | [optional] 

## Example

```python
from mudbase.models.project_sms_byo_public import ProjectSmsByoPublic

# TODO update the JSON string below
json = "{}"
# create an instance of ProjectSmsByoPublic from a JSON string
project_sms_byo_public_instance = ProjectSmsByoPublic.from_json(json)
# print the JSON string representation of the object
print(ProjectSmsByoPublic.to_json())

# convert the object into a dict
project_sms_byo_public_dict = project_sms_byo_public_instance.to_dict()
# create an instance of ProjectSmsByoPublic from a dict
project_sms_byo_public_from_dict = ProjectSmsByoPublic.from_dict(project_sms_byo_public_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


