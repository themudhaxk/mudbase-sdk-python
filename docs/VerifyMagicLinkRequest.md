# VerifyMagicLinkRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**token** | **str** |  | 

## Example

```python
from mudbase.models.verify_magic_link_request import VerifyMagicLinkRequest

# TODO update the JSON string below
json = "{}"
# create an instance of VerifyMagicLinkRequest from a JSON string
verify_magic_link_request_instance = VerifyMagicLinkRequest.from_json(json)
# print the JSON string representation of the object
print(VerifyMagicLinkRequest.to_json())

# convert the object into a dict
verify_magic_link_request_dict = verify_magic_link_request_instance.to_dict()
# create an instance of VerifyMagicLinkRequest from a dict
verify_magic_link_request_from_dict = VerifyMagicLinkRequest.from_dict(verify_magic_link_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


