# GetActiveUsers200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**users** | [**List[GetActiveUsers200ResponseUsersInner]**](GetActiveUsers200ResponseUsersInner.md) |  | [optional] 
**count** | **int** |  | [optional] 
**timestamp** | **datetime** |  | [optional] 

## Example

```python
from mudbase.models.get_active_users200_response import GetActiveUsers200Response

# TODO update the JSON string below
json = "{}"
# create an instance of GetActiveUsers200Response from a JSON string
get_active_users200_response_instance = GetActiveUsers200Response.from_json(json)
# print the JSON string representation of the object
print(GetActiveUsers200Response.to_json())

# convert the object into a dict
get_active_users200_response_dict = get_active_users200_response_instance.to_dict()
# create an instance of GetActiveUsers200Response from a dict
get_active_users200_response_from_dict = GetActiveUsers200Response.from_dict(get_active_users200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


