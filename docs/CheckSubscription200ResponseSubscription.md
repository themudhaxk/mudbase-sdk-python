# CheckSubscription200ResponseSubscription


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**status** | **str** |  | [optional] 
**plan** | **str** |  | [optional] 

## Example

```python
from mudbase.models.check_subscription200_response_subscription import CheckSubscription200ResponseSubscription

# TODO update the JSON string below
json = "{}"
# create an instance of CheckSubscription200ResponseSubscription from a JSON string
check_subscription200_response_subscription_instance = CheckSubscription200ResponseSubscription.from_json(json)
# print the JSON string representation of the object
print(CheckSubscription200ResponseSubscription.to_json())

# convert the object into a dict
check_subscription200_response_subscription_dict = check_subscription200_response_subscription_instance.to_dict()
# create an instance of CheckSubscription200ResponseSubscription from a dict
check_subscription200_response_subscription_from_dict = CheckSubscription200ResponseSubscription.from_dict(check_subscription200_response_subscription_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


