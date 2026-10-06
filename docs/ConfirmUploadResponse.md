# ConfirmUploadResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**file_id** | **str** |  | [optional] 
**status** | **str** |  | [optional] 
**scan** | [**ConfirmUploadResponseScan**](ConfirmUploadResponseScan.md) |  | [optional] 

## Example

```python
from mudbase.models.confirm_upload_response import ConfirmUploadResponse

# TODO update the JSON string below
json = "{}"
# create an instance of ConfirmUploadResponse from a JSON string
confirm_upload_response_instance = ConfirmUploadResponse.from_json(json)
# print the JSON string representation of the object
print(ConfirmUploadResponse.to_json())

# convert the object into a dict
confirm_upload_response_dict = confirm_upload_response_instance.to_dict()
# create an instance of ConfirmUploadResponse from a dict
confirm_upload_response_from_dict = ConfirmUploadResponse.from_dict(confirm_upload_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


