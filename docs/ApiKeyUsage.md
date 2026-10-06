# ApiKeyUsage


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**requests** | **int** |  | [optional] 
**last_used** | **datetime** |  | [optional] 

## Example

```python
from mudbase.models.api_key_usage import ApiKeyUsage

# TODO update the JSON string below
json = "{}"
# create an instance of ApiKeyUsage from a JSON string
api_key_usage_instance = ApiKeyUsage.from_json(json)
# print the JSON string representation of the object
print(ApiKeyUsage.to_json())

# convert the object into a dict
api_key_usage_dict = api_key_usage_instance.to_dict()
# create an instance of ApiKeyUsage from a dict
api_key_usage_from_dict = ApiKeyUsage.from_dict(api_key_usage_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


