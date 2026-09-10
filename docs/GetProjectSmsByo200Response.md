# GetProjectSmsByo200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**success** | **bool** |  | [optional] 
**data** | [**ProjectSmsByoPublic**](ProjectSmsByoPublic.md) |  | [optional] 

## Example

```python
from mudbase.models.get_project_sms_byo200_response import GetProjectSmsByo200Response

# TODO update the JSON string below
json = "{}"
# create an instance of GetProjectSmsByo200Response from a JSON string
get_project_sms_byo200_response_instance = GetProjectSmsByo200Response.from_json(json)
# print the JSON string representation of the object
print(GetProjectSmsByo200Response.to_json())

# convert the object into a dict
get_project_sms_byo200_response_dict = get_project_sms_byo200_response_instance.to_dict()
# create an instance of GetProjectSmsByo200Response from a dict
get_project_sms_byo200_response_from_dict = GetProjectSmsByo200Response.from_dict(get_project_sms_byo200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


