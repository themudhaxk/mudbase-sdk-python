# VerifyOrgPlanPayment200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**success** | **bool** |  | [optional] 
**message** | **str** |  | [optional] 
**data** | [**VerifyOrgPlanPayment200ResponseData**](VerifyOrgPlanPayment200ResponseData.md) |  | [optional] 

## Example

```python
from mudbase.models.verify_org_plan_payment200_response import VerifyOrgPlanPayment200Response

# TODO update the JSON string below
json = "{}"
# create an instance of VerifyOrgPlanPayment200Response from a JSON string
verify_org_plan_payment200_response_instance = VerifyOrgPlanPayment200Response.from_json(json)
# print the JSON string representation of the object
print(VerifyOrgPlanPayment200Response.to_json())

# convert the object into a dict
verify_org_plan_payment200_response_dict = verify_org_plan_payment200_response_instance.to_dict()
# create an instance of VerifyOrgPlanPayment200Response from a dict
verify_org_plan_payment200_response_from_dict = VerifyOrgPlanPayment200Response.from_dict(verify_org_plan_payment200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


