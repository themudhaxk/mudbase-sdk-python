# CheckUserPresence200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**presence** | [**Dict[str, CheckUserPresence200ResponsePresenceValue]**](CheckUserPresence200ResponsePresenceValue.md) |  | [optional] 
**timestamp** | **datetime** |  | [optional] 

## Example

```python
from mudbase.models.check_user_presence200_response import CheckUserPresence200Response

# TODO update the JSON string below
json = "{}"
# create an instance of CheckUserPresence200Response from a JSON string
check_user_presence200_response_instance = CheckUserPresence200Response.from_json(json)
# print the JSON string representation of the object
print(CheckUserPresence200Response.to_json())

# convert the object into a dict
check_user_presence200_response_dict = check_user_presence200_response_instance.to_dict()
# create an instance of CheckUserPresence200Response from a dict
check_user_presence200_response_from_dict = CheckUserPresence200Response.from_dict(check_user_presence200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


