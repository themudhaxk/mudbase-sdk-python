# AdminBillingCheckoutLinkRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**plan** | **str** |  | 
**billing_cycle** | **str** |  | [optional] [default to 'monthly']
**amount_cents** | **int** | Monthly amount in cents (overrides catalog; enterprise default is contract) | [optional] 
**charge_amount_cents** | **int** | Exact charge in cents for this checkout (overrides monthly math) | [optional] 
**currency** | **str** |  | [optional] 
**email** | **str** |  | [optional] 
**name** | **str** |  | [optional] 
**redirect_url** | **str** |  | [optional] 
**send_email** | **bool** |  | [optional] [default to False]
**to_email** | **str** |  | [optional] 
**message** | **str** | Optional note shown in org_billing_checkout email | [optional] 

## Example

```python
from mudbase.models.admin_billing_checkout_link_request import AdminBillingCheckoutLinkRequest

# TODO update the JSON string below
json = "{}"
# create an instance of AdminBillingCheckoutLinkRequest from a JSON string
admin_billing_checkout_link_request_instance = AdminBillingCheckoutLinkRequest.from_json(json)
# print the JSON string representation of the object
print(AdminBillingCheckoutLinkRequest.to_json())

# convert the object into a dict
admin_billing_checkout_link_request_dict = admin_billing_checkout_link_request_instance.to_dict()
# create an instance of AdminBillingCheckoutLinkRequest from a dict
admin_billing_checkout_link_request_from_dict = AdminBillingCheckoutLinkRequest.from_dict(admin_billing_checkout_link_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


