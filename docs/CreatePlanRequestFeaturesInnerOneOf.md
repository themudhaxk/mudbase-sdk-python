# CreatePlanRequestFeaturesInnerOneOf


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** |  | [optional] 
**description** | **str** |  | [optional] 
**included** | **bool** |  | [optional] [default to True]
**limit** | **float** | Usage cap for this feature; omit or null for unlimited. | [optional] 

## Example

```python
from mudbase.models.create_plan_request_features_inner_one_of import CreatePlanRequestFeaturesInnerOneOf

# TODO update the JSON string below
json = "{}"
# create an instance of CreatePlanRequestFeaturesInnerOneOf from a JSON string
create_plan_request_features_inner_one_of_instance = CreatePlanRequestFeaturesInnerOneOf.from_json(json)
# print the JSON string representation of the object
print(CreatePlanRequestFeaturesInnerOneOf.to_json())

# convert the object into a dict
create_plan_request_features_inner_one_of_dict = create_plan_request_features_inner_one_of_instance.to_dict()
# create an instance of CreatePlanRequestFeaturesInnerOneOf from a dict
create_plan_request_features_inner_one_of_from_dict = CreatePlanRequestFeaturesInnerOneOf.from_dict(create_plan_request_features_inner_one_of_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


