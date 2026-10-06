# UpdateOrganizationPlan200ResponseOneOf


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**message** | **str** |  | [optional] 
**org** | [**Organization**](Organization.md) |  | [optional] 

## Example

```python
from mudbase.models.update_organization_plan200_response_one_of import UpdateOrganizationPlan200ResponseOneOf

# TODO update the JSON string below
json = "{}"
# create an instance of UpdateOrganizationPlan200ResponseOneOf from a JSON string
update_organization_plan200_response_one_of_instance = UpdateOrganizationPlan200ResponseOneOf.from_json(json)
# print the JSON string representation of the object
print(UpdateOrganizationPlan200ResponseOneOf.to_json())

# convert the object into a dict
update_organization_plan200_response_one_of_dict = update_organization_plan200_response_one_of_instance.to_dict()
# create an instance of UpdateOrganizationPlan200ResponseOneOf from a dict
update_organization_plan200_response_one_of_from_dict = UpdateOrganizationPlan200ResponseOneOf.from_dict(update_organization_plan200_response_one_of_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


