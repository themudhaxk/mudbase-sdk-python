# SimulateAppPermissionsRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**role** | **str** | App role slug (same as &#x60;roleSlug&#x60; elsewhere) | 
**role_slug** | **str** | Alias for &#x60;role&#x60; | [optional] 
**operation_id** | **str** | OpenAPI operationId (e.g. &#x60;sendEmail&#x60;, &#x60;executeIntegration&#x60;). When set, path simulation is optional. | [optional] 
**method** | **str** |  | [optional] 
**pathname** | **str** | Full path e.g. &#x60;/api/messaging/projects/{id}/messaging/email&#x60; | [optional] 
**path** | **str** | Alias for &#x60;pathname&#x60; | [optional] 

## Example

```python
from mudbase.models.simulate_app_permissions_request import SimulateAppPermissionsRequest

# TODO update the JSON string below
json = "{}"
# create an instance of SimulateAppPermissionsRequest from a JSON string
simulate_app_permissions_request_instance = SimulateAppPermissionsRequest.from_json(json)
# print the JSON string representation of the object
print(SimulateAppPermissionsRequest.to_json())

# convert the object into a dict
simulate_app_permissions_request_dict = simulate_app_permissions_request_instance.to_dict()
# create an instance of SimulateAppPermissionsRequest from a dict
simulate_app_permissions_request_from_dict = SimulateAppPermissionsRequest.from_dict(simulate_app_permissions_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


