# CreateChat201ResponseData


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** |  | [optional] 
**name** | **str** |  | [optional] 
**type** | **str** |  | [optional] 
**participants** | **List[str]** |  | [optional] 
**created_at** | **datetime** |  | [optional] 

## Example

```python
from mudbase.models.create_chat201_response_data import CreateChat201ResponseData

# TODO update the JSON string below
json = "{}"
# create an instance of CreateChat201ResponseData from a JSON string
create_chat201_response_data_instance = CreateChat201ResponseData.from_json(json)
# print the JSON string representation of the object
print(CreateChat201ResponseData.to_json())

# convert the object into a dict
create_chat201_response_data_dict = create_chat201_response_data_instance.to_dict()
# create an instance of CreateChat201ResponseData from a dict
create_chat201_response_data_from_dict = CreateChat201ResponseData.from_dict(create_chat201_response_data_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


