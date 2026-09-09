# EditMessage200ResponseData


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** |  | [optional] 
**content** | **str** |  | [optional] 
**is_e2ee** | **bool** |  | [optional] 
**e2ee** | **object** |  | [optional] 
**edited_at** | **str** |  | [optional] 

## Example

```python
from mudbase.models.edit_message200_response_data import EditMessage200ResponseData

# TODO update the JSON string below
json = "{}"
# create an instance of EditMessage200ResponseData from a JSON string
edit_message200_response_data_instance = EditMessage200ResponseData.from_json(json)
# print the JSON string representation of the object
print(EditMessage200ResponseData.to_json())

# convert the object into a dict
edit_message200_response_data_dict = edit_message200_response_data_instance.to_dict()
# create an instance of EditMessage200ResponseData from a dict
edit_message200_response_data_from_dict = EditMessage200ResponseData.from_dict(edit_message200_response_data_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


