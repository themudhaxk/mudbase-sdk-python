# CheckUserPresence200ResponsePresenceValue


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**online** | **bool** |  | [optional] 
**last_seen** | **datetime** |  | [optional] 

## Example

```python
from mudbase.models.check_user_presence200_response_presence_value import CheckUserPresence200ResponsePresenceValue

# TODO update the JSON string below
json = "{}"
# create an instance of CheckUserPresence200ResponsePresenceValue from a JSON string
check_user_presence200_response_presence_value_instance = CheckUserPresence200ResponsePresenceValue.from_json(json)
# print the JSON string representation of the object
print(CheckUserPresence200ResponsePresenceValue.to_json())

# convert the object into a dict
check_user_presence200_response_presence_value_dict = check_user_presence200_response_presence_value_instance.to_dict()
# create an instance of CheckUserPresence200ResponsePresenceValue from a dict
check_user_presence200_response_presence_value_from_dict = CheckUserPresence200ResponsePresenceValue.from_dict(check_user_presence200_response_presence_value_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


