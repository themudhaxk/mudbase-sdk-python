# ConvertAnonymousAccount200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**message** | **str** |  | [optional] 
**token** | **str** |  | [optional] 
**refresh_token** | **str** |  | [optional] 
**expires_in** | **int** |  | [optional] 
**user** | [**User**](User.md) |  | [optional] 

## Example

```python
from mudbase.models.convert_anonymous_account200_response import ConvertAnonymousAccount200Response

# TODO update the JSON string below
json = "{}"
# create an instance of ConvertAnonymousAccount200Response from a JSON string
convert_anonymous_account200_response_instance = ConvertAnonymousAccount200Response.from_json(json)
# print the JSON string representation of the object
print(ConvertAnonymousAccount200Response.to_json())

# convert the object into a dict
convert_anonymous_account200_response_dict = convert_anonymous_account200_response_instance.to_dict()
# create an instance of ConvertAnonymousAccount200Response from a dict
convert_anonymous_account200_response_from_dict = ConvertAnonymousAccount200Response.from_dict(convert_anonymous_account200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


