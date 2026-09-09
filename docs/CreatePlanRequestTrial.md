# CreatePlanRequestTrial

Defaults to `{ enabled: false, days: 7 }` when omitted.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**enabled** | **bool** |  | [optional] 
**days** | **float** |  | [optional] 

## Example

```python
from mudbase.models.create_plan_request_trial import CreatePlanRequestTrial

# TODO update the JSON string below
json = "{}"
# create an instance of CreatePlanRequestTrial from a JSON string
create_plan_request_trial_instance = CreatePlanRequestTrial.from_json(json)
# print the JSON string representation of the object
print(CreatePlanRequestTrial.to_json())

# convert the object into a dict
create_plan_request_trial_dict = create_plan_request_trial_instance.to_dict()
# create an instance of CreatePlanRequestTrial from a dict
create_plan_request_trial_from_dict = CreatePlanRequestTrial.from_dict(create_plan_request_trial_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


