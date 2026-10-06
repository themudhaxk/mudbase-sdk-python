# RequestPasswordResetRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**email** | **str** |  | 

## Example

```python
from mudbase.models.request_password_reset_request import RequestPasswordResetRequest

# TODO update the JSON string below
json = "{}"
# create an instance of RequestPasswordResetRequest from a JSON string
request_password_reset_request_instance = RequestPasswordResetRequest.from_json(json)
# print the JSON string representation of the object
print(RequestPasswordResetRequest.to_json())

# convert the object into a dict
request_password_reset_request_dict = request_password_reset_request_instance.to_dict()
# create an instance of RequestPasswordResetRequest from a dict
request_password_reset_request_from_dict = RequestPasswordResetRequest.from_dict(request_password_reset_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


