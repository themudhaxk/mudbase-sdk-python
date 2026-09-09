# CreateCheckoutSessionRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**plan_id** | **str** | Plan ID to subscribe to | 
**billing_cycle** | **str** | Billing interval | 
**customer_info** | [**CreateCheckoutSessionRequestCustomerInfo**](CreateCheckoutSessionRequestCustomerInfo.md) |  | 
**success_url** | **str** | Redirect URL after successful payment | [optional] 
**cancel_url** | **str** | Redirect URL if user cancels | [optional] 

## Example

```python
from mudbase.models.create_checkout_session_request import CreateCheckoutSessionRequest

# TODO update the JSON string below
json = "{}"
# create an instance of CreateCheckoutSessionRequest from a JSON string
create_checkout_session_request_instance = CreateCheckoutSessionRequest.from_json(json)
# print the JSON string representation of the object
print(CreateCheckoutSessionRequest.to_json())

# convert the object into a dict
create_checkout_session_request_dict = create_checkout_session_request_instance.to_dict()
# create an instance of CreateCheckoutSessionRequest from a dict
create_checkout_session_request_from_dict = CreateCheckoutSessionRequest.from_dict(create_checkout_session_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


