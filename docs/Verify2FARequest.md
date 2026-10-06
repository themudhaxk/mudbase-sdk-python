# Verify2FARequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**token** | **str** |  | 

## Example

```python
from mudbase.models.verify2_fa_request import Verify2FARequest

# TODO update the JSON string below
json = "{}"
# create an instance of Verify2FARequest from a JSON string
verify2_fa_request_instance = Verify2FARequest.from_json(json)
# print the JSON string representation of the object
print(Verify2FARequest.to_json())

# convert the object into a dict
verify2_fa_request_dict = verify2_fa_request_instance.to_dict()
# create an instance of Verify2FARequest from a dict
verify2_fa_request_from_dict = Verify2FARequest.from_dict(verify2_fa_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


