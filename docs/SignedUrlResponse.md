# SignedUrlResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**success** | **bool** |  | [optional] 
**url** | **str** | Signed URL for file access | [optional] 
**expires_at** | **datetime** | Expiration time of the signed URL (optional - some endpoints return expiresIn instead) | [optional] 
**expires_in** | **int** | Time-to-live in seconds for the signed URL (optional) | [optional] 

## Example

```python
from mudbase.models.signed_url_response import SignedUrlResponse

# TODO update the JSON string below
json = "{}"
# create an instance of SignedUrlResponse from a JSON string
signed_url_response_instance = SignedUrlResponse.from_json(json)
# print the JSON string representation of the object
print(SignedUrlResponse.to_json())

# convert the object into a dict
signed_url_response_dict = signed_url_response_instance.to_dict()
# create an instance of SignedUrlResponse from a dict
signed_url_response_from_dict = SignedUrlResponse.from_dict(signed_url_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


