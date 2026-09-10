# GetOverage200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**overage** | [**List[GetOverage200ResponseOverageInner]**](GetOverage200ResponseOverageInner.md) |  | [optional] 

## Example

```python
from mudbase.models.get_overage200_response import GetOverage200Response

# TODO update the JSON string below
json = "{}"
# create an instance of GetOverage200Response from a JSON string
get_overage200_response_instance = GetOverage200Response.from_json(json)
# print the JSON string representation of the object
print(GetOverage200Response.to_json())

# convert the object into a dict
get_overage200_response_dict = get_overage200_response_instance.to_dict()
# create an instance of GetOverage200Response from a dict
get_overage200_response_from_dict = GetOverage200Response.from_dict(get_overage200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


