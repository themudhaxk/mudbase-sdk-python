# CreatePlan201Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**message** | **str** |  | [optional] 
**plan** | [**Plan**](Plan.md) |  | [optional] 

## Example

```python
from mudbase.models.create_plan201_response import CreatePlan201Response

# TODO update the JSON string below
json = "{}"
# create an instance of CreatePlan201Response from a JSON string
create_plan201_response_instance = CreatePlan201Response.from_json(json)
# print the JSON string representation of the object
print(CreatePlan201Response.to_json())

# convert the object into a dict
create_plan201_response_dict = create_plan201_response_instance.to_dict()
# create an instance of CreatePlan201Response from a dict
create_plan201_response_from_dict = CreatePlan201Response.from_dict(create_plan201_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


