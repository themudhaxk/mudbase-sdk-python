# HealthResponseServices


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**database** | **str** |  | [optional] 
**redis** | **str** |  | [optional] 
**storage** | **str** |  | [optional] 
**email** | **str** |  | [optional] 
**sms** | **str** |  | [optional] 

## Example

```python
from mudbase.models.health_response_services import HealthResponseServices

# TODO update the JSON string below
json = "{}"
# create an instance of HealthResponseServices from a JSON string
health_response_services_instance = HealthResponseServices.from_json(json)
# print the JSON string representation of the object
print(HealthResponseServices.to_json())

# convert the object into a dict
health_response_services_dict = health_response_services_instance.to_dict()
# create an instance of HealthResponseServices from a dict
health_response_services_from_dict = HealthResponseServices.from_dict(health_response_services_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


