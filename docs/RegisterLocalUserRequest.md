# RegisterLocalUserRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**email** | **str** |  | 
**password** | **str** |  | 
**first_name** | **str** |  | 
**last_name** | **str** |  | 
**project_id** | **str** |  | 

## Example

```python
from mudbase.models.register_local_user_request import RegisterLocalUserRequest

# TODO update the JSON string below
json = "{}"
# create an instance of RegisterLocalUserRequest from a JSON string
register_local_user_request_instance = RegisterLocalUserRequest.from_json(json)
# print the JSON string representation of the object
print(RegisterLocalUserRequest.to_json())

# convert the object into a dict
register_local_user_request_dict = register_local_user_request_instance.to_dict()
# create an instance of RegisterLocalUserRequest from a dict
register_local_user_request_from_dict = RegisterLocalUserRequest.from_dict(register_local_user_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


