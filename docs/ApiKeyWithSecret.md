# ApiKeyWithSecret


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** |  | [optional] 
**name** | **str** |  | [optional] 
**project** | [**ProjectSummary**](ProjectSummary.md) |  | [optional] 
**permissions** | [**List[ApiKeyPermission]**](ApiKeyPermission.md) |  | [optional] 
**rate_limit** | [**RateLimit**](RateLimit.md) |  | [optional] 
**usage** | [**ApiKeyUsage**](ApiKeyUsage.md) |  | [optional] 
**is_active** | **bool** |  | [optional] 
**expires_at** | **datetime** |  | [optional] 
**created_by** | [**UserSummary**](UserSummary.md) |  | [optional] 
**created_at** | **datetime** |  | [optional] 
**secret** | **str** |  | [optional] 

## Example

```python
from mudbase.models.api_key_with_secret import ApiKeyWithSecret

# TODO update the JSON string below
json = "{}"
# create an instance of ApiKeyWithSecret from a JSON string
api_key_with_secret_instance = ApiKeyWithSecret.from_json(json)
# print the JSON string representation of the object
print(ApiKeyWithSecret.to_json())

# convert the object into a dict
api_key_with_secret_dict = api_key_with_secret_instance.to_dict()
# create an instance of ApiKeyWithSecret from a dict
api_key_with_secret_from_dict = ApiKeyWithSecret.from_dict(api_key_with_secret_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


