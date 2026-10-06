# MagicLinkRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**email** | **str** |  | 
**project_id** | **str** |  | 
**redirect_url** | **str** |  | [optional] 

## Example

```python
from mudbase.models.magic_link_request import MagicLinkRequest

# TODO update the JSON string below
json = "{}"
# create an instance of MagicLinkRequest from a JSON string
magic_link_request_instance = MagicLinkRequest.from_json(json)
# print the JSON string representation of the object
print(MagicLinkRequest.to_json())

# convert the object into a dict
magic_link_request_dict = magic_link_request_instance.to_dict()
# create an instance of MagicLinkRequest from a dict
magic_link_request_from_dict = MagicLinkRequest.from_dict(magic_link_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


