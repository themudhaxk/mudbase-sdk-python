# GetMultiRoleConfig200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**success** | **bool** |  | [optional] 
**data** | [**GetMultiRoleConfig200ResponseData**](GetMultiRoleConfig200ResponseData.md) |  | [optional] 

## Example

```python
from mudbase.models.get_multi_role_config200_response import GetMultiRoleConfig200Response

# TODO update the JSON string below
json = "{}"
# create an instance of GetMultiRoleConfig200Response from a JSON string
get_multi_role_config200_response_instance = GetMultiRoleConfig200Response.from_json(json)
# print the JSON string representation of the object
print(GetMultiRoleConfig200Response.to_json())

# convert the object into a dict
get_multi_role_config200_response_dict = get_multi_role_config200_response_instance.to_dict()
# create an instance of GetMultiRoleConfig200Response from a dict
get_multi_role_config200_response_from_dict = GetMultiRoleConfig200Response.from_dict(get_multi_role_config200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


