# ApiProjectsProjectIdKybSessionsPostRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**workflow_id** | **str** | Overrides the organization&#39;s default KYB workflow. | [optional] 
**vendor_business_id** | **str** | Your own identifier for the business being verified. | [optional] 
**vendor_data** | **str** | Arbitrary reference echoed back on webhooks. | [optional] 
**callback** | **str** | Where to redirect the business user after the hosted flow. | [optional] 
**language** | **str** |  | [optional] 

## Example

```python
from mudbase.models.api_projects_project_id_kyb_sessions_post_request import ApiProjectsProjectIdKybSessionsPostRequest

# TODO update the JSON string below
json = "{}"
# create an instance of ApiProjectsProjectIdKybSessionsPostRequest from a JSON string
api_projects_project_id_kyb_sessions_post_request_instance = ApiProjectsProjectIdKybSessionsPostRequest.from_json(json)
# print the JSON string representation of the object
print(ApiProjectsProjectIdKybSessionsPostRequest.to_json())

# convert the object into a dict
api_projects_project_id_kyb_sessions_post_request_dict = api_projects_project_id_kyb_sessions_post_request_instance.to_dict()
# create an instance of ApiProjectsProjectIdKybSessionsPostRequest from a dict
api_projects_project_id_kyb_sessions_post_request_from_dict = ApiProjectsProjectIdKybSessionsPostRequest.from_dict(api_projects_project_id_kyb_sessions_post_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


