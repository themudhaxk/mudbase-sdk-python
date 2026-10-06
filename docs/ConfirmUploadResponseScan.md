# ConfirmUploadResponseScan

Virus scan result (provider, status, detections, raw analysis)

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**status** | **str** |  | [optional] 
**provider** | **str** |  | [optional] 
**detections** | **int** |  | [optional] 
**analysis** | **object** | Raw analysis object returned by the scanner (e.g., VirusTotal) | [optional] 

## Example

```python
from mudbase.models.confirm_upload_response_scan import ConfirmUploadResponseScan

# TODO update the JSON string below
json = "{}"
# create an instance of ConfirmUploadResponseScan from a JSON string
confirm_upload_response_scan_instance = ConfirmUploadResponseScan.from_json(json)
# print the JSON string representation of the object
print(ConfirmUploadResponseScan.to_json())

# convert the object into a dict
confirm_upload_response_scan_dict = confirm_upload_response_scan_instance.to_dict()
# create an instance of ConfirmUploadResponseScan from a dict
confirm_upload_response_scan_from_dict = ConfirmUploadResponseScan.from_dict(confirm_upload_response_scan_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


