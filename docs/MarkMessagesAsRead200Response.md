# MarkMessagesAsRead200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**success** | **bool** |  | [optional] 
**data** | [**MarkMessagesAsRead200ResponseData**](MarkMessagesAsRead200ResponseData.md) |  | [optional] 

## Example

```python
from mudbase.models.mark_messages_as_read200_response import MarkMessagesAsRead200Response

# TODO update the JSON string below
json = "{}"
# create an instance of MarkMessagesAsRead200Response from a JSON string
mark_messages_as_read200_response_instance = MarkMessagesAsRead200Response.from_json(json)
# print the JSON string representation of the object
print(MarkMessagesAsRead200Response.to_json())

# convert the object into a dict
mark_messages_as_read200_response_dict = mark_messages_as_read200_response_instance.to_dict()
# create an instance of MarkMessagesAsRead200Response from a dict
mark_messages_as_read200_response_from_dict = MarkMessagesAsRead200Response.from_dict(mark_messages_as_read200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


