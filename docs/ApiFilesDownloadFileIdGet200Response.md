# ApiFilesDownloadFileIdGet200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**url** | **str** |  | [optional] 
**expires_in** | **int** | Seconds until the signed URL expires; null for public files. | [optional] 
**is_public** | **bool** | Present and true only when the file is public. | [optional] 
**warning** | **str** | Present only for public files — explains the URL is permanent and unprotected. | [optional] 

## Example

```python
from mudbase.models.api_files_download_file_id_get200_response import ApiFilesDownloadFileIdGet200Response

# TODO update the JSON string below
json = "{}"
# create an instance of ApiFilesDownloadFileIdGet200Response from a JSON string
api_files_download_file_id_get200_response_instance = ApiFilesDownloadFileIdGet200Response.from_json(json)
# print the JSON string representation of the object
print(ApiFilesDownloadFileIdGet200Response.to_json())

# convert the object into a dict
api_files_download_file_id_get200_response_dict = api_files_download_file_id_get200_response_instance.to_dict()
# create an instance of ApiFilesDownloadFileIdGet200Response from a dict
api_files_download_file_id_get200_response_from_dict = ApiFilesDownloadFileIdGet200Response.from_dict(api_files_download_file_id_get200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


