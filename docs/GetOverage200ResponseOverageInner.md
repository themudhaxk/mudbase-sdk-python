# GetOverage200ResponseOverageInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**resource** | **str** | e.g. storage, apiCalls, realtimeMessages | [optional] 
**units** | **float** |  | [optional] 
**amount** | **float** |  | [optional] 
**currency** | **str** |  | [optional] 
**unit** | **str** |  | [optional] 

## Example

```python
from mudbase.models.get_overage200_response_overage_inner import GetOverage200ResponseOverageInner

# TODO update the JSON string below
json = "{}"
# create an instance of GetOverage200ResponseOverageInner from a JSON string
get_overage200_response_overage_inner_instance = GetOverage200ResponseOverageInner.from_json(json)
# print the JSON string representation of the object
print(GetOverage200ResponseOverageInner.to_json())

# convert the object into a dict
get_overage200_response_overage_inner_dict = get_overage200_response_overage_inner_instance.to_dict()
# create an instance of GetOverage200ResponseOverageInner from a dict
get_overage200_response_overage_inner_from_dict = GetOverage200ResponseOverageInner.from_dict(get_overage200_response_overage_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


