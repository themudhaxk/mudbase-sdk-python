# SimulateAppPermissions200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**success** | **bool** |  | [optional] 
**allowed** | **bool** |  | [optional] 
**reason** | **str** |  | [optional] 
**evaluated** | [**SimulateAppPermissions200ResponseEvaluated**](SimulateAppPermissions200ResponseEvaluated.md) |  | [optional] 

## Example

```python
from mudbase.models.simulate_app_permissions200_response import SimulateAppPermissions200Response

# TODO update the JSON string below
json = "{}"
# create an instance of SimulateAppPermissions200Response from a JSON string
simulate_app_permissions200_response_instance = SimulateAppPermissions200Response.from_json(json)
# print the JSON string representation of the object
print(SimulateAppPermissions200Response.to_json())

# convert the object into a dict
simulate_app_permissions200_response_dict = simulate_app_permissions200_response_instance.to_dict()
# create an instance of SimulateAppPermissions200Response from a dict
simulate_app_permissions200_response_from_dict = SimulateAppPermissions200Response.from_dict(simulate_app_permissions200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


