# CreateCollection201Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**message** | **str** |  | [optional] 
**collection** | [**Collection**](Collection.md) |  | [optional] 

## Example

```python
from mudbase.models.create_collection201_response import CreateCollection201Response

# TODO update the JSON string below
json = "{}"
# create an instance of CreateCollection201Response from a JSON string
create_collection201_response_instance = CreateCollection201Response.from_json(json)
# print the JSON string representation of the object
print(CreateCollection201Response.to_json())

# convert the object into a dict
create_collection201_response_dict = create_collection201_response_instance.to_dict()
# create an instance of CreateCollection201Response from a dict
create_collection201_response_from_dict = CreateCollection201Response.from_dict(create_collection201_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


