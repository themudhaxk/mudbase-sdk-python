# GetProjectFcmConfig200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**success** | **bool** |  | [optional] 
**data** | [**GetProjectFcmConfig200ResponseData**](GetProjectFcmConfig200ResponseData.md) |  | [optional] 

## Example

```python
from mudbase.models.get_project_fcm_config200_response import GetProjectFcmConfig200Response

# TODO update the JSON string below
json = "{}"
# create an instance of GetProjectFcmConfig200Response from a JSON string
get_project_fcm_config200_response_instance = GetProjectFcmConfig200Response.from_json(json)
# print the JSON string representation of the object
print(GetProjectFcmConfig200Response.to_json())

# convert the object into a dict
get_project_fcm_config200_response_dict = get_project_fcm_config200_response_instance.to_dict()
# create an instance of GetProjectFcmConfig200Response from a dict
get_project_fcm_config200_response_from_dict = GetProjectFcmConfig200Response.from_dict(get_project_fcm_config200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


