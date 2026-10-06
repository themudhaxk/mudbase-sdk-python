# UploadFiles413Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**error** | **str** |  | [optional] 
**max_file_upload_bytes** | **int** |  | [optional] 

## Example

```python
from mudbase.models.upload_files413_response import UploadFiles413Response

# TODO update the JSON string below
json = "{}"
# create an instance of UploadFiles413Response from a JSON string
upload_files413_response_instance = UploadFiles413Response.from_json(json)
# print the JSON string representation of the object
print(UploadFiles413Response.to_json())

# convert the object into a dict
upload_files413_response_dict = upload_files413_response_instance.to_dict()
# create an instance of UploadFiles413Response from a dict
upload_files413_response_from_dict = UploadFiles413Response.from_dict(upload_files413_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


