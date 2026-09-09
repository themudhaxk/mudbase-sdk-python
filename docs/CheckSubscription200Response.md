# CheckSubscription200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**has_subscription** | **bool** |  | [optional] 
**subscription** | [**CheckSubscription200ResponseSubscription**](CheckSubscription200ResponseSubscription.md) |  | [optional] 

## Example

```python
from mudbase.models.check_subscription200_response import CheckSubscription200Response

# TODO update the JSON string below
json = "{}"
# create an instance of CheckSubscription200Response from a JSON string
check_subscription200_response_instance = CheckSubscription200Response.from_json(json)
# print the JSON string representation of the object
print(CheckSubscription200Response.to_json())

# convert the object into a dict
check_subscription200_response_dict = check_subscription200_response_instance.to_dict()
# create an instance of CheckSubscription200Response from a dict
check_subscription200_response_from_dict = CheckSubscription200Response.from_dict(check_subscription200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


