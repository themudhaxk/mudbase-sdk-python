# ConfirmDirectUploadRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**key** | **str** | The object key returned when the presigned PUT URL was issued | 
**project_id** | **str** |  | 
**original_name** | **str** |  | [optional] 
**content_type** | **str** |  | [optional] 
**size** | **int** |  | [optional] 
**bucket** | **str** |  | [optional] 
**is_public** | **bool** |  | [optional] 

## Example

```python
from mudbase.models.confirm_direct_upload_request import ConfirmDirectUploadRequest

# TODO update the JSON string below
json = "{}"
# create an instance of ConfirmDirectUploadRequest from a JSON string
confirm_direct_upload_request_instance = ConfirmDirectUploadRequest.from_json(json)
# print the JSON string representation of the object
print(ConfirmDirectUploadRequest.to_json())

# convert the object into a dict
confirm_direct_upload_request_dict = confirm_direct_upload_request_instance.to_dict()
# create an instance of ConfirmDirectUploadRequest from a dict
confirm_direct_upload_request_from_dict = ConfirmDirectUploadRequest.from_dict(confirm_direct_upload_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


