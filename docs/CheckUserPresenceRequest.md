# CheckUserPresenceRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**user_ids** | **List[str]** |  | 

## Example

```python
from mudbase.models.check_user_presence_request import CheckUserPresenceRequest

# TODO update the JSON string below
json = "{}"
# create an instance of CheckUserPresenceRequest from a JSON string
check_user_presence_request_instance = CheckUserPresenceRequest.from_json(json)
# print the JSON string representation of the object
print(CheckUserPresenceRequest.to_json())

# convert the object into a dict
check_user_presence_request_dict = check_user_presence_request_instance.to_dict()
# create an instance of CheckUserPresenceRequest from a dict
check_user_presence_request_from_dict = CheckUserPresenceRequest.from_dict(check_user_presence_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


