# BillingLastPayment


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**amount** | **float** |  | [optional] 
**var_date** | **datetime** |  | [optional] 
**status** | **str** |  | [optional] 

## Example

```python
from mudbase.models.billing_last_payment import BillingLastPayment

# TODO update the JSON string below
json = "{}"
# create an instance of BillingLastPayment from a JSON string
billing_last_payment_instance = BillingLastPayment.from_json(json)
# print the JSON string representation of the object
print(BillingLastPayment.to_json())

# convert the object into a dict
billing_last_payment_dict = billing_last_payment_instance.to_dict()
# create an instance of BillingLastPayment from a dict
billing_last_payment_from_dict = BillingLastPayment.from_dict(billing_last_payment_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


