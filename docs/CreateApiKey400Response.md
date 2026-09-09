# CreateApiKey400Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**error** | **str** |  | [optional] 
**details** | **List[str]** |  | [optional] 

## Example

```python
from mudbase.models.create_api_key400_response import CreateApiKey400Response

# TODO update the JSON string below
json = "{}"
# create an instance of CreateApiKey400Response from a JSON string
create_api_key400_response_instance = CreateApiKey400Response.from_json(json)
# print the JSON string representation of the object
print(CreateApiKey400Response.to_json())

# convert the object into a dict
create_api_key400_response_dict = create_api_key400_response_instance.to_dict()
# create an instance of CreateApiKey400Response from a dict
create_api_key400_response_from_dict = CreateApiKey400Response.from_dict(create_api_key400_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


