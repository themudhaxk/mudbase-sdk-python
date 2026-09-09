# ApiKycWorkflowsGet200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**workflows** | [**List[ApiKycWorkflowsGet200ResponseWorkflowsInner]**](ApiKycWorkflowsGet200ResponseWorkflowsInner.md) |  | [optional] 
**kyc** | **List[object]** |  | [optional] 
**kyb** | **List[object]** |  | [optional] 

## Example

```python
from mudbase.models.api_kyc_workflows_get200_response import ApiKycWorkflowsGet200Response

# TODO update the JSON string below
json = "{}"
# create an instance of ApiKycWorkflowsGet200Response from a JSON string
api_kyc_workflows_get200_response_instance = ApiKycWorkflowsGet200Response.from_json(json)
# print the JSON string representation of the object
print(ApiKycWorkflowsGet200Response.to_json())

# convert the object into a dict
api_kyc_workflows_get200_response_dict = api_kyc_workflows_get200_response_instance.to_dict()
# create an instance of ApiKycWorkflowsGet200Response from a dict
api_kyc_workflows_get200_response_from_dict = ApiKycWorkflowsGet200Response.from_dict(api_kyc_workflows_get200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


