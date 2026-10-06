# SendMessage201Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**success** | **bool** |  | [optional] 
**data** | [**SendMessage201ResponseData**](SendMessage201ResponseData.md) |  | [optional] 

## Example

```python
from mudbase.models.send_message201_response import SendMessage201Response

# TODO update the JSON string below
json = "{}"
# create an instance of SendMessage201Response from a JSON string
send_message201_response_instance = SendMessage201Response.from_json(json)
# print the JSON string representation of the object
print(SendMessage201Response.to_json())

# convert the object into a dict
send_message201_response_dict = send_message201_response_instance.to_dict()
# create an instance of SendMessage201Response from a dict
send_message201_response_from_dict = SendMessage201Response.from_dict(send_message201_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


