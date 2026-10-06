# EnqueueProjectEmail202Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**success** | **bool** |  | [optional] 
**job_id** | **str** |  | [optional] 

## Example

```python
from mudbase.models.enqueue_project_email202_response import EnqueueProjectEmail202Response

# TODO update the JSON string below
json = "{}"
# create an instance of EnqueueProjectEmail202Response from a JSON string
enqueue_project_email202_response_instance = EnqueueProjectEmail202Response.from_json(json)
# print the JSON string representation of the object
print(EnqueueProjectEmail202Response.to_json())

# convert the object into a dict
enqueue_project_email202_response_dict = enqueue_project_email202_response_instance.to_dict()
# create an instance of EnqueueProjectEmail202Response from a dict
enqueue_project_email202_response_from_dict = EnqueueProjectEmail202Response.from_dict(enqueue_project_email202_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


