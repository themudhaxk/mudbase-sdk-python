# GetUsersByRole200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**users** | **List[object]** |  | [optional] 
**total** | **int** |  | [optional] 

## Example

```python
from mudbase.models.get_users_by_role200_response import GetUsersByRole200Response

# TODO update the JSON string below
json = "{}"
# create an instance of GetUsersByRole200Response from a JSON string
get_users_by_role200_response_instance = GetUsersByRole200Response.from_json(json)
# print the JSON string representation of the object
print(GetUsersByRole200Response.to_json())

# convert the object into a dict
get_users_by_role200_response_dict = get_users_by_role200_response_instance.to_dict()
# create an instance of GetUsersByRole200Response from a dict
get_users_by_role200_response_from_dict = GetUsersByRole200Response.from_dict(get_users_by_role200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


