# GenerateSignedUrlRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**expires_in** | **int** |  | [optional] [default to 3600]

## Example

```python
from mudbase.models.generate_signed_url_request import GenerateSignedUrlRequest

# TODO update the JSON string below
json = "{}"
# create an instance of GenerateSignedUrlRequest from a JSON string
generate_signed_url_request_instance = GenerateSignedUrlRequest.from_json(json)
# print the JSON string representation of the object
print(GenerateSignedUrlRequest.to_json())

# convert the object into a dict
generate_signed_url_request_dict = generate_signed_url_request_instance.to_dict()
# create an instance of GenerateSignedUrlRequest from a dict
generate_signed_url_request_from_dict = GenerateSignedUrlRequest.from_dict(generate_signed_url_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


