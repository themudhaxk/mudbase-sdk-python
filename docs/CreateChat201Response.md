# CreateChat201Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**success** | **bool** |  | [optional] 
**data** | [**CreateChat201ResponseData**](CreateChat201ResponseData.md) |  | [optional] 

## Example

```python
from mudbase.models.create_chat201_response import CreateChat201Response

# TODO update the JSON string below
json = "{}"
# create an instance of CreateChat201Response from a JSON string
create_chat201_response_instance = CreateChat201Response.from_json(json)
# print the JSON string representation of the object
print(CreateChat201Response.to_json())

# convert the object into a dict
create_chat201_response_dict = create_chat201_response_instance.to_dict()
# create an instance of CreateChat201Response from a dict
create_chat201_response_from_dict = CreateChat201Response.from_dict(create_chat201_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


