# Organization


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** |  | [optional] 
**name** | **str** |  | [optional] 
**slug** | **str** |  | [optional] 
**description** | **str** |  | [optional] 
**logo** | **str** | Optional logo URL. Org-related emails use the platform logo (env); this field is for legacy or future UI use only. | [optional] 
**website** | **str** |  | [optional] 
**plan** | [**Plan**](Plan.md) |  | [optional] 
**usage** | [**Usage**](Usage.md) |  | [optional] 
**limits** | [**Limits**](Limits.md) |  | [optional] 
**billing** | [**Billing**](Billing.md) |  | [optional] 
**settings** | **object** | May include customDomainAddon (optional billing/legacy flag; not required for custom domains on Growth/Scale). | [optional] 
**deployment_type** | **str** |  | [optional] 
**dedicated** | **object** | Dedicated API/DB routing; may include edgeTlsStatus, infraMeteringLastReportAt. | [optional] 
**preferred_region** | **str** |  | [optional] 
**infrastructure_environments** | **List[object]** |  | [optional] 
**allowed_domains** | **List[object]** |  | [optional] 
**created_at** | **datetime** |  | [optional] 
**updated_at** | **datetime** |  | [optional] 

## Example

```python
from mudbase.models.organization import Organization

# TODO update the JSON string below
json = "{}"
# create an instance of Organization from a JSON string
organization_instance = Organization.from_json(json)
# print the JSON string representation of the object
print(Organization.to_json())

# convert the object into a dict
organization_dict = organization_instance.to_dict()
# create an instance of Organization from a dict
organization_from_dict = Organization.from_dict(organization_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


