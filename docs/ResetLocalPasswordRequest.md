# ResetLocalPasswordRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**password** | **str** |  | 
**project_id** | **str** |  | [optional] 

## Example

```python
from mudbase.models.reset_local_password_request import ResetLocalPasswordRequest

# TODO update the JSON string below
json = "{}"
# create an instance of ResetLocalPasswordRequest from a JSON string
reset_local_password_request_instance = ResetLocalPasswordRequest.from_json(json)
# print the JSON string representation of the object
print(ResetLocalPasswordRequest.to_json())

# convert the object into a dict
reset_local_password_request_dict = reset_local_password_request_instance.to_dict()
# create an instance of ResetLocalPasswordRequest from a dict
reset_local_password_request_from_dict = ResetLocalPasswordRequest.from_dict(reset_local_password_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


