# RequestLocalPasswordResetRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**email** | **str** |  | 
**project_id** | **str** | Required for project-based reset (sends OTP). Omit for org token link. | [optional] 

## Example

```python
from mudbase.models.request_local_password_reset_request import RequestLocalPasswordResetRequest

# TODO update the JSON string below
json = "{}"
# create an instance of RequestLocalPasswordResetRequest from a JSON string
request_local_password_reset_request_instance = RequestLocalPasswordResetRequest.from_json(json)
# print the JSON string representation of the object
print(RequestLocalPasswordResetRequest.to_json())

# convert the object into a dict
request_local_password_reset_request_dict = request_local_password_reset_request_instance.to_dict()
# create an instance of RequestLocalPasswordResetRequest from a dict
request_local_password_reset_request_from_dict = RequestLocalPasswordResetRequest.from_dict(request_local_password_reset_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


