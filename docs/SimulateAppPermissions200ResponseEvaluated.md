# SimulateAppPermissions200ResponseEvaluated


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**role** | **str** |  | [optional] 
**method** | **str** |  | [optional] 
**pathname** | **str** |  | [optional] 
**operation_id** | **str** |  | [optional] 
**resource** | **str** |  | [optional] 
**action** | **str** |  | [optional] 

## Example

```python
from mudbase.models.simulate_app_permissions200_response_evaluated import SimulateAppPermissions200ResponseEvaluated

# TODO update the JSON string below
json = "{}"
# create an instance of SimulateAppPermissions200ResponseEvaluated from a JSON string
simulate_app_permissions200_response_evaluated_instance = SimulateAppPermissions200ResponseEvaluated.from_json(json)
# print the JSON string representation of the object
print(SimulateAppPermissions200ResponseEvaluated.to_json())

# convert the object into a dict
simulate_app_permissions200_response_evaluated_dict = simulate_app_permissions200_response_evaluated_instance.to_dict()
# create an instance of SimulateAppPermissions200ResponseEvaluated from a dict
simulate_app_permissions200_response_evaluated_from_dict = SimulateAppPermissions200ResponseEvaluated.from_dict(simulate_app_permissions200_response_evaluated_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


