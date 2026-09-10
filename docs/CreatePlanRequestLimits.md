# CreatePlanRequestLimits

Plan caps; null or omitted fields mean unlimited where applicable.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**api_calls** | **float** |  | [optional] 
**storage** | **float** |  | [optional] 
**bandwidth** | **float** |  | [optional] 
**users** | **float** |  | [optional] 
**custom_limits** | [**List[CreatePlanRequestLimitsCustomLimitsInner]**](CreatePlanRequestLimitsCustomLimitsInner.md) |  | [optional] 

## Example

```python
from mudbase.models.create_plan_request_limits import CreatePlanRequestLimits

# TODO update the JSON string below
json = "{}"
# create an instance of CreatePlanRequestLimits from a JSON string
create_plan_request_limits_instance = CreatePlanRequestLimits.from_json(json)
# print the JSON string representation of the object
print(CreatePlanRequestLimits.to_json())

# convert the object into a dict
create_plan_request_limits_dict = create_plan_request_limits_instance.to_dict()
# create an instance of CreatePlanRequestLimits from a dict
create_plan_request_limits_from_dict = CreatePlanRequestLimits.from_dict(create_plan_request_limits_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


