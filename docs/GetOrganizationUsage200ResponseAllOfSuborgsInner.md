# GetOrganizationUsage200ResponseAllOfSuborgsInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** |  | [optional] 
**name** | **str** |  | [optional] 
**slug** | **str** |  | [optional] 
**usage** | [**Usage**](Usage.md) |  | [optional] 

## Example

```python
from mudbase.models.get_organization_usage200_response_all_of_suborgs_inner import GetOrganizationUsage200ResponseAllOfSuborgsInner

# TODO update the JSON string below
json = "{}"
# create an instance of GetOrganizationUsage200ResponseAllOfSuborgsInner from a JSON string
get_organization_usage200_response_all_of_suborgs_inner_instance = GetOrganizationUsage200ResponseAllOfSuborgsInner.from_json(json)
# print the JSON string representation of the object
print(GetOrganizationUsage200ResponseAllOfSuborgsInner.to_json())

# convert the object into a dict
get_organization_usage200_response_all_of_suborgs_inner_dict = get_organization_usage200_response_all_of_suborgs_inner_instance.to_dict()
# create an instance of GetOrganizationUsage200ResponseAllOfSuborgsInner from a dict
get_organization_usage200_response_all_of_suborgs_inner_from_dict = GetOrganizationUsage200ResponseAllOfSuborgsInner.from_dict(get_organization_usage200_response_all_of_suborgs_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


