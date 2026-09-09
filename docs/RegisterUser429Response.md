# RegisterUser429Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**error** | **str** |  | [optional] 
**code** | **str** |  | [optional] 
**details** | [**ErrorDetails**](ErrorDetails.md) |  | [optional] 
**timestamp** | **datetime** |  | [optional] 
**path** | **str** |  | [optional] 
**request_id** | **str** |  | [optional] 
**retry_after** | **int** |  | [optional] 

## Example

```python
from mudbase.models.register_user429_response import RegisterUser429Response

# TODO update the JSON string below
json = "{}"
# create an instance of RegisterUser429Response from a JSON string
register_user429_response_instance = RegisterUser429Response.from_json(json)
# print the JSON string representation of the object
print(RegisterUser429Response.to_json())

# convert the object into a dict
register_user429_response_dict = register_user429_response_instance.to_dict()
# create an instance of RegisterUser429Response from a dict
register_user429_response_from_dict = RegisterUser429Response.from_dict(register_user429_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


