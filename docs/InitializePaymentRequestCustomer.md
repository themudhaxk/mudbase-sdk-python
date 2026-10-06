# InitializePaymentRequestCustomer


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**email** | **str** |  | 
**name** | **str** |  | [optional] 

## Example

```python
from mudbase.models.initialize_payment_request_customer import InitializePaymentRequestCustomer

# TODO update the JSON string below
json = "{}"
# create an instance of InitializePaymentRequestCustomer from a JSON string
initialize_payment_request_customer_instance = InitializePaymentRequestCustomer.from_json(json)
# print the JSON string representation of the object
print(InitializePaymentRequestCustomer.to_json())

# convert the object into a dict
initialize_payment_request_customer_dict = initialize_payment_request_customer_instance.to_dict()
# create an instance of InitializePaymentRequestCustomer from a dict
initialize_payment_request_customer_from_dict = InitializePaymentRequestCustomer.from_dict(initialize_payment_request_customer_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


