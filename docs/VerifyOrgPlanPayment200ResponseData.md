# VerifyOrgPlanPayment200ResponseData


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**plan** | **str** | New plan name (e.g. starter) | [optional] 
**billing_cycle** | **str** |  | [optional] 
**org_id** | **str** |  | [optional] 

## Example

```python
from mudbase.models.verify_org_plan_payment200_response_data import VerifyOrgPlanPayment200ResponseData

# TODO update the JSON string below
json = "{}"
# create an instance of VerifyOrgPlanPayment200ResponseData from a JSON string
verify_org_plan_payment200_response_data_instance = VerifyOrgPlanPayment200ResponseData.from_json(json)
# print the JSON string representation of the object
print(VerifyOrgPlanPayment200ResponseData.to_json())

# convert the object into a dict
verify_org_plan_payment200_response_data_dict = verify_org_plan_payment200_response_data_instance.to_dict()
# create an instance of VerifyOrgPlanPayment200ResponseData from a dict
verify_org_plan_payment200_response_data_from_dict = VerifyOrgPlanPayment200ResponseData.from_dict(verify_org_plan_payment200_response_data_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


