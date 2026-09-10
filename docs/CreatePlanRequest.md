# CreatePlanRequest

OpenAPI-style body normalized server-side into Plan.pricing (monthly/yearly amounts), features (objects with name/included), and optional limits/trial/metadata. Slug is derived from projectId + name unless a collision occurs. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** | Display name; also used to generate a unique slug per project. | 
**description** | **str** |  | [optional] 
**price** | **float** | Amount for the chosen interval. The server fills the other billing period (e.g. yearly ≈ monthly × 12 × 0.8 when interval is month).  | 
**currency** | **str** | ISO currency code (stored lowercased). | 
**interval** | **str** | Which period &#x60;price&#x60; applies to; drives pricing.monthly vs pricing.yearly. | 
**features** | [**List[CreatePlanRequestFeaturesInner]**](CreatePlanRequestFeaturesInner.md) | Strings become &#x60;{ name, included: true }&#x60;. You may send full feature objects instead.  | [optional] 
**limits** | [**CreatePlanRequestLimits**](CreatePlanRequestLimits.md) |  | [optional] 
**trial** | [**CreatePlanRequestTrial**](CreatePlanRequestTrial.md) |  | [optional] 
**is_active** | **bool** |  | [optional] [default to True]
**is_default** | **bool** | Only one default plan per project is allowed server-side. | [optional] [default to False]
**sort_order** | **float** | Lower numbers list first in UIs. | [optional] 
**metadata** | **Dict[str, object]** | Arbitrary key/value data stored on the plan document. | [optional] 

## Example

```python
from mudbase.models.create_plan_request import CreatePlanRequest

# TODO update the JSON string below
json = "{}"
# create an instance of CreatePlanRequest from a JSON string
create_plan_request_instance = CreatePlanRequest.from_json(json)
# print the JSON string representation of the object
print(CreatePlanRequest.to_json())

# convert the object into a dict
create_plan_request_dict = create_plan_request_instance.to_dict()
# create an instance of CreatePlanRequest from a dict
create_plan_request_from_dict = CreatePlanRequest.from_dict(create_plan_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


