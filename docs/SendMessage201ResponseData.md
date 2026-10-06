# SendMessage201ResponseData


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** |  | [optional] 
**content** | **str** |  | [optional] 
**sender** | **str** |  | [optional] 
**created_at** | **datetime** |  | [optional] 

## Example

```python
from mudbase.models.send_message201_response_data import SendMessage201ResponseData

# TODO update the JSON string below
json = "{}"
# create an instance of SendMessage201ResponseData from a JSON string
send_message201_response_data_instance = SendMessage201ResponseData.from_json(json)
# print the JSON string representation of the object
print(SendMessage201ResponseData.to_json())

# convert the object into a dict
send_message201_response_data_dict = send_message201_response_data_instance.to_dict()
# create an instance of SendMessage201ResponseData from a dict
send_message201_response_data_from_dict = SendMessage201ResponseData.from_dict(send_message201_response_data_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


