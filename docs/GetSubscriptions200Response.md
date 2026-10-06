# GetSubscriptions200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**subscriptions** | [**List[GetSubscriptions200ResponseSubscriptionsInner]**](GetSubscriptions200ResponseSubscriptionsInner.md) |  | [optional] 

## Example

```python
from mudbase.models.get_subscriptions200_response import GetSubscriptions200Response

# TODO update the JSON string below
json = "{}"
# create an instance of GetSubscriptions200Response from a JSON string
get_subscriptions200_response_instance = GetSubscriptions200Response.from_json(json)
# print the JSON string representation of the object
print(GetSubscriptions200Response.to_json())

# convert the object into a dict
get_subscriptions200_response_dict = get_subscriptions200_response_instance.to_dict()
# create an instance of GetSubscriptions200Response from a dict
get_subscriptions200_response_from_dict = GetSubscriptions200Response.from_dict(get_subscriptions200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


