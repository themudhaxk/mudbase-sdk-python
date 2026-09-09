# ApiKey


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

## Example

```python
from mudbase.models.api_key import ApiKey

# TODO update the JSON string below
json = "{}"
# create an instance of ApiKey from a JSON string
api_key_instance = ApiKey.from_json(json)
# print the JSON string representation of the object
print(ApiKey.to_json())

# convert the object into a dict
api_key_dict = api_key_instance.to_dict()
# create an instance of ApiKey from a dict
api_key_from_dict = ApiKey.from_dict(api_key_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


