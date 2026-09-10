# UpdateOrganizationPlan200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**message** | **str** |  | [optional] 
**org** | [**Organization**](Organization.md) |  | [optional] 
**error** | **str** |  | [optional] 

## Example

```python
from mudbase.models.update_organization_plan200_response import UpdateOrganizationPlan200Response

# TODO update the JSON string below
json = "{}"
# create an instance of UpdateOrganizationPlan200Response from a JSON string
update_organization_plan200_response_instance = UpdateOrganizationPlan200Response.from_json(json)
# print the JSON string representation of the object
print(UpdateOrganizationPlan200Response.to_json())

# convert the object into a dict
update_organization_plan200_response_dict = update_organization_plan200_response_instance.to_dict()
# create an instance of UpdateOrganizationPlan200Response from a dict
update_organization_plan200_response_from_dict = UpdateOrganizationPlan200Response.from_dict(update_organization_plan200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


