# CreateCheckoutSessionRequestCustomerInfo


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**email** | **str** |  | 
**name** | **str** |  | [optional] 

## Example

```python
from mudbase.models.create_checkout_session_request_customer_info import CreateCheckoutSessionRequestCustomerInfo

# TODO update the JSON string below
json = "{}"
# create an instance of CreateCheckoutSessionRequestCustomerInfo from a JSON string
create_checkout_session_request_customer_info_instance = CreateCheckoutSessionRequestCustomerInfo.from_json(json)
# print the JSON string representation of the object
print(CreateCheckoutSessionRequestCustomerInfo.to_json())

# convert the object into a dict
create_checkout_session_request_customer_info_dict = create_checkout_session_request_customer_info_instance.to_dict()
# create an instance of CreateCheckoutSessionRequestCustomerInfo from a dict
create_checkout_session_request_customer_info_from_dict = CreateCheckoutSessionRequestCustomerInfo.from_dict(create_checkout_session_request_customer_info_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


