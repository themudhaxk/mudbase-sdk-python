# Disable2FARequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**password** | **str** |  | 
**token** | **str** |  | 

## Example

```python
from mudbase.models.disable2_fa_request import Disable2FARequest

# TODO update the JSON string below
json = "{}"
# create an instance of Disable2FARequest from a JSON string
disable2_fa_request_instance = Disable2FARequest.from_json(json)
# print the JSON string representation of the object
print(Disable2FARequest.to_json())

# convert the object into a dict
disable2_fa_request_dict = disable2_fa_request_instance.to_dict()
# create an instance of Disable2FARequest from a dict
disable2_fa_request_from_dict = Disable2FARequest.from_dict(disable2_fa_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


