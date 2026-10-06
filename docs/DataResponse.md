# DataResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**message** | **str** |  | [optional] 
**data** | **object** |  | [optional] 

## Example

```python
from mudbase.models.data_response import DataResponse

# TODO update the JSON string below
json = "{}"
# create an instance of DataResponse from a JSON string
data_response_instance = DataResponse.from_json(json)
# print the JSON string representation of the object
print(DataResponse.to_json())

# convert the object into a dict
data_response_dict = data_response_instance.to_dict()
# create an instance of DataResponse from a dict
data_response_from_dict = DataResponse.from_dict(data_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


