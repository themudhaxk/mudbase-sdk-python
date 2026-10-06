# VerifyPayment200ResponseDataSubscription


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** |  | [optional] 
**status** | **str** |  | [optional] 
**plan** | **str** |  | [optional] 
**current_period_end** | **datetime** |  | [optional] 

## Example

```python
from mudbase.models.verify_payment200_response_data_subscription import VerifyPayment200ResponseDataSubscription

# TODO update the JSON string below
json = "{}"
# create an instance of VerifyPayment200ResponseDataSubscription from a JSON string
verify_payment200_response_data_subscription_instance = VerifyPayment200ResponseDataSubscription.from_json(json)
# print the JSON string representation of the object
print(VerifyPayment200ResponseDataSubscription.to_json())

# convert the object into a dict
verify_payment200_response_data_subscription_dict = verify_payment200_response_data_subscription_instance.to_dict()
# create an instance of VerifyPayment200ResponseDataSubscription from a dict
verify_payment200_response_data_subscription_from_dict = VerifyPayment200ResponseDataSubscription.from_dict(verify_payment200_response_data_subscription_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


