# GetDashboard200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**revenue** | **float** |  | [optional] 
**subscriptions** | **int** |  | [optional] 
**active_plans** | **int** |  | [optional] 

## Example

```python
from mudbase.models.get_dashboard200_response import GetDashboard200Response

# TODO update the JSON string below
json = "{}"
# create an instance of GetDashboard200Response from a JSON string
get_dashboard200_response_instance = GetDashboard200Response.from_json(json)
# print the JSON string representation of the object
print(GetDashboard200Response.to_json())

# convert the object into a dict
get_dashboard200_response_dict = get_dashboard200_response_instance.to_dict()
# create an instance of GetDashboard200Response from a dict
get_dashboard200_response_from_dict = GetDashboard200Response.from_dict(get_dashboard200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


