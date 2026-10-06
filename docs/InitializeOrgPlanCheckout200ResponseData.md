# InitializeOrgPlanCheckout200ResponseData


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**link** | **str** | Payment URL | [optional] 
**tx_ref** | **str** | Reference for verify-payment (mudbase_org_...) | [optional] 
**provider_ref** | **str** |  | [optional] 
**billing_cycle** | **str** |  | [optional] 
**amount** | **float** |  | [optional] 
**amount_cents** | **float** |  | [optional] 

## Example

```python
from mudbase.models.initialize_org_plan_checkout200_response_data import InitializeOrgPlanCheckout200ResponseData

# TODO update the JSON string below
json = "{}"
# create an instance of InitializeOrgPlanCheckout200ResponseData from a JSON string
initialize_org_plan_checkout200_response_data_instance = InitializeOrgPlanCheckout200ResponseData.from_json(json)
# print the JSON string representation of the object
print(InitializeOrgPlanCheckout200ResponseData.to_json())

# convert the object into a dict
initialize_org_plan_checkout200_response_data_dict = initialize_org_plan_checkout200_response_data_instance.to_dict()
# create an instance of InitializeOrgPlanCheckout200ResponseData from a dict
initialize_org_plan_checkout200_response_data_from_dict = InitializeOrgPlanCheckout200ResponseData.from_dict(initialize_org_plan_checkout200_response_data_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


