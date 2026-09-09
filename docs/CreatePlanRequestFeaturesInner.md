# CreatePlanRequestFeaturesInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** |  | [optional] 
**description** | **str** |  | [optional] 
**included** | **bool** |  | [optional] [default to True]
**limit** | **float** | Usage cap for this feature; omit or null for unlimited. | [optional] 

## Example

```python
from mudbase.models.create_plan_request_features_inner import CreatePlanRequestFeaturesInner

# TODO update the JSON string below
json = "{}"
# create an instance of CreatePlanRequestFeaturesInner from a JSON string
create_plan_request_features_inner_instance = CreatePlanRequestFeaturesInner.from_json(json)
# print the JSON string representation of the object
print(CreatePlanRequestFeaturesInner.to_json())

# convert the object into a dict
create_plan_request_features_inner_dict = create_plan_request_features_inner_instance.to_dict()
# create an instance of CreatePlanRequestFeaturesInner from a dict
create_plan_request_features_inner_from_dict = CreatePlanRequestFeaturesInner.from_dict(create_plan_request_features_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


