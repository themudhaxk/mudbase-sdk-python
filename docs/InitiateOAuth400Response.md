# InitiateOAuth400Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**error** | **str** |  | [optional] 

## Example

```python
from mudbase.models.initiate_o_auth400_response import InitiateOAuth400Response

# TODO update the JSON string below
json = "{}"
# create an instance of InitiateOAuth400Response from a JSON string
initiate_o_auth400_response_instance = InitiateOAuth400Response.from_json(json)
# print the JSON string representation of the object
print(InitiateOAuth400Response.to_json())

# convert the object into a dict
initiate_o_auth400_response_dict = initiate_o_auth400_response_instance.to_dict()
# create an instance of InitiateOAuth400Response from a dict
initiate_o_auth400_response_from_dict = InitiateOAuth400Response.from_dict(initiate_o_auth400_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


