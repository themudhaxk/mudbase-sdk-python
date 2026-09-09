# DownloadInvoice200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**url** | **str** |  | [optional] 
**message** | **str** |  | [optional] 

## Example

```python
from mudbase.models.download_invoice200_response import DownloadInvoice200Response

# TODO update the JSON string below
json = "{}"
# create an instance of DownloadInvoice200Response from a JSON string
download_invoice200_response_instance = DownloadInvoice200Response.from_json(json)
# print the JSON string representation of the object
print(DownloadInvoice200Response.to_json())

# convert the object into a dict
download_invoice200_response_dict = download_invoice200_response_instance.to_dict()
# create an instance of DownloadInvoice200Response from a dict
download_invoice200_response_from_dict = DownloadInvoice200Response.from_dict(download_invoice200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


