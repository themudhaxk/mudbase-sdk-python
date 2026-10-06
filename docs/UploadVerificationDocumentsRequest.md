# UploadVerificationDocumentsRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**role_slug** | **str** |  | 
**documents** | [**List[UploadVerificationDocumentsRequestDocumentsInner]**](UploadVerificationDocumentsRequestDocumentsInner.md) |  | 

## Example

```python
from mudbase.models.upload_verification_documents_request import UploadVerificationDocumentsRequest

# TODO update the JSON string below
json = "{}"
# create an instance of UploadVerificationDocumentsRequest from a JSON string
upload_verification_documents_request_instance = UploadVerificationDocumentsRequest.from_json(json)
# print the JSON string representation of the object
print(UploadVerificationDocumentsRequest.to_json())

# convert the object into a dict
upload_verification_documents_request_dict = upload_verification_documents_request_instance.to_dict()
# create an instance of UploadVerificationDocumentsRequest from a dict
upload_verification_documents_request_from_dict = UploadVerificationDocumentsRequest.from_dict(upload_verification_documents_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


