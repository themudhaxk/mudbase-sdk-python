# GeneratePresignedUploadRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**project_id** | **str** |  | 
**bucket** | **str** |  | [optional] [default to 'default']
**original_name** | **str** |  | 
**content_type** | **str** |  | [optional] 
**is_public** | **bool** |  | [optional] [default to False]

## Example

```python
from mudbase.models.generate_presigned_upload_request import GeneratePresignedUploadRequest

# TODO update the JSON string below
json = "{}"
# create an instance of GeneratePresignedUploadRequest from a JSON string
generate_presigned_upload_request_instance = GeneratePresignedUploadRequest.from_json(json)
# print the JSON string representation of the object
print(GeneratePresignedUploadRequest.to_json())

# convert the object into a dict
generate_presigned_upload_request_dict = generate_presigned_upload_request_instance.to_dict()
# create an instance of GeneratePresignedUploadRequest from a dict
generate_presigned_upload_request_from_dict = GeneratePresignedUploadRequest.from_dict(generate_presigned_upload_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


