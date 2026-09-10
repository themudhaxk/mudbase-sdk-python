# InitializePaymentRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**amount** | **float** | Payment amount (e.g. USD) | 
**currency** | **str** |  | [optional] [default to 'USD']
**project_id** | **str** | Optional project scope | [optional] 
**customer** | [**InitializePaymentRequestCustomer**](InitializePaymentRequestCustomer.md) |  | 
**metadata** | **object** | title, description, redirectUrl, etc. | [optional] 

## Example

```python
from mudbase.models.initialize_payment_request import InitializePaymentRequest

# TODO update the JSON string below
json = "{}"
# create an instance of InitializePaymentRequest from a JSON string
initialize_payment_request_instance = InitializePaymentRequest.from_json(json)
# print the JSON string representation of the object
print(InitializePaymentRequest.to_json())

# convert the object into a dict
initialize_payment_request_dict = initialize_payment_request_instance.to_dict()
# create an instance of InitializePaymentRequest from a dict
initialize_payment_request_from_dict = InitializePaymentRequest.from_dict(initialize_payment_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


