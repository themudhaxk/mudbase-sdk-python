# PresignedPostResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**key** | **str** | Object key clients should upload to | [optional] 
**url** | **str** | Presigned URL to PUT the file body to directly | [optional] 
**method** | **str** | HTTP method the client must use against &#x60;url&#x60; (always PUT - the object storage backend does not implement a POST-based upload API) | [optional] 
**headers** | **object** | Headers the client must send with the PUT request (e.g. Content-Type) - mismatching these from what was signed causes a SignatureDoesNotMatch error | [optional] 
**expires_in** | **int** | Expiration of the presigned URL in seconds | [optional] 
**max_file_upload_bytes** | **int** | Maximum upload size in bytes for this org plan. Not enforced by the presigned URL itself (PUT has no content-length-range equivalent) - checked server-side by /api/files/upload/confirm after the upload completes | [optional] 

## Example

```python
from mudbase.models.presigned_post_response import PresignedPostResponse

# TODO update the JSON string below
json = "{}"
# create an instance of PresignedPostResponse from a JSON string
presigned_post_response_instance = PresignedPostResponse.from_json(json)
# print the JSON string representation of the object
print(PresignedPostResponse.to_json())

# convert the object into a dict
presigned_post_response_dict = presigned_post_response_instance.to_dict()
# create an instance of PresignedPostResponse from a dict
presigned_post_response_from_dict = PresignedPostResponse.from_dict(presigned_post_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


