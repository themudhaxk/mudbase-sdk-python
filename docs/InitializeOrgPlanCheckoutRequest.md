# InitializeOrgPlanCheckoutRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**plan_name** | **str** | Plan id from GET /api/billing/plans (excludes free and enterprise) | 
**billing_cycle** | **str** | Yearly &#x3D; 2 months free (~16.67% discount) | [optional] [default to 'monthly']
**redirect_url** | **str** | Override redirect after payment (default FRONTEND_URL/billing/callback) | [optional] 

## Example

```python
from mudbase.models.initialize_org_plan_checkout_request import InitializeOrgPlanCheckoutRequest

# TODO update the JSON string below
json = "{}"
# create an instance of InitializeOrgPlanCheckoutRequest from a JSON string
initialize_org_plan_checkout_request_instance = InitializeOrgPlanCheckoutRequest.from_json(json)
# print the JSON string representation of the object
print(InitializeOrgPlanCheckoutRequest.to_json())

# convert the object into a dict
initialize_org_plan_checkout_request_dict = initialize_org_plan_checkout_request_instance.to_dict()
# create an instance of InitializeOrgPlanCheckoutRequest from a dict
initialize_org_plan_checkout_request_from_dict = InitializeOrgPlanCheckoutRequest.from_dict(initialize_org_plan_checkout_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


