# GetProjectFeeDashboard200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**success** | **bool** |  | [optional] 
**data** | [**GetProjectFeeDashboard200ResponseData**](GetProjectFeeDashboard200ResponseData.md) |  | [optional] 

## Example

```python
from mudbase.models.get_project_fee_dashboard200_response import GetProjectFeeDashboard200Response

# TODO update the JSON string below
json = "{}"
# create an instance of GetProjectFeeDashboard200Response from a JSON string
get_project_fee_dashboard200_response_instance = GetProjectFeeDashboard200Response.from_json(json)
# print the JSON string representation of the object
print(GetProjectFeeDashboard200Response.to_json())

# convert the object into a dict
get_project_fee_dashboard200_response_dict = get_project_fee_dashboard200_response_instance.to_dict()
# create an instance of GetProjectFeeDashboard200Response from a dict
get_project_fee_dashboard200_response_from_dict = GetProjectFeeDashboard200Response.from_dict(get_project_fee_dashboard200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


