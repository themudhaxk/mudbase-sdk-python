# GetPlans200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**plans** | [**List[Plan]**](Plan.md) |  | [optional] 
**total** | **int** |  | [optional] 

## Example

```python
from mudbase.models.get_plans200_response import GetPlans200Response

# TODO update the JSON string below
json = "{}"
# create an instance of GetPlans200Response from a JSON string
get_plans200_response_instance = GetPlans200Response.from_json(json)
# print the JSON string representation of the object
print(GetPlans200Response.to_json())

# convert the object into a dict
get_plans200_response_dict = get_plans200_response_instance.to_dict()
# create an instance of GetPlans200Response from a dict
get_plans200_response_from_dict = GetPlans200Response.from_dict(get_plans200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


