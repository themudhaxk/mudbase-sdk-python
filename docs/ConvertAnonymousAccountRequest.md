# ConvertAnonymousAccountRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**email** | **str** |  | 
**password** | **str** |  | 
**first_name** | **str** |  | [optional] 
**last_name** | **str** |  | [optional] 

## Example

```python
from mudbase.models.convert_anonymous_account_request import ConvertAnonymousAccountRequest

# TODO update the JSON string below
json = "{}"
# create an instance of ConvertAnonymousAccountRequest from a JSON string
convert_anonymous_account_request_instance = ConvertAnonymousAccountRequest.from_json(json)
# print the JSON string representation of the object
print(ConvertAnonymousAccountRequest.to_json())

# convert the object into a dict
convert_anonymous_account_request_dict = convert_anonymous_account_request_instance.to_dict()
# create an instance of ConvertAnonymousAccountRequest from a dict
convert_anonymous_account_request_from_dict = ConvertAnonymousAccountRequest.from_dict(convert_anonymous_account_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


