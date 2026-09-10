# UploadProjectLogo200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**logo_url** | **str** |  | [optional] 
**project** | [**Project**](Project.md) |  | [optional] 

## Example

```python
from mudbase.models.upload_project_logo200_response import UploadProjectLogo200Response

# TODO update the JSON string below
json = "{}"
# create an instance of UploadProjectLogo200Response from a JSON string
upload_project_logo200_response_instance = UploadProjectLogo200Response.from_json(json)
# print the JSON string representation of the object
print(UploadProjectLogo200Response.to_json())

# convert the object into a dict
upload_project_logo200_response_dict = upload_project_logo200_response_instance.to_dict()
# create an instance of UploadProjectLogo200Response from a dict
upload_project_logo200_response_from_dict = UploadProjectLogo200Response.from_dict(upload_project_logo200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


