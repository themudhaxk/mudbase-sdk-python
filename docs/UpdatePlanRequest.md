# UpdatePlanRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** |  | [optional] 
**description** | **str** |  | [optional] 
**price** | **float** |  | [optional] 
**features** | **List[str]** |  | [optional] 

## Example

```python
from mudbase.models.update_plan_request import UpdatePlanRequest

# TODO update the JSON string below
json = "{}"
# create an instance of UpdatePlanRequest from a JSON string
update_plan_request_instance = UpdatePlanRequest.from_json(json)
# print the JSON string representation of the object
print(UpdatePlanRequest.to_json())

# convert the object into a dict
update_plan_request_dict = update_plan_request_instance.to_dict()
# create an instance of UpdatePlanRequest from a dict
update_plan_request_from_dict = UpdatePlanRequest.from_dict(update_plan_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


