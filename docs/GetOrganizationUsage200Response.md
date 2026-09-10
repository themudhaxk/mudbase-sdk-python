# GetOrganizationUsage200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**usage** | [**Usage**](Usage.md) |  | [optional] 
**limits** | [**Limits**](Limits.md) |  | [optional] 
**plan** | [**Plan**](Plan.md) |  | [optional] 
**billing** | [**Billing**](Billing.md) |  | [optional] 
**suborgs** | [**List[GetOrganizationUsage200ResponseAllOfSuborgsInner]**](GetOrganizationUsage200ResponseAllOfSuborgsInner.md) |  | [optional] 

## Example

```python
from mudbase.models.get_organization_usage200_response import GetOrganizationUsage200Response

# TODO update the JSON string below
json = "{}"
# create an instance of GetOrganizationUsage200Response from a JSON string
get_organization_usage200_response_instance = GetOrganizationUsage200Response.from_json(json)
# print the JSON string representation of the object
print(GetOrganizationUsage200Response.to_json())

# convert the object into a dict
get_organization_usage200_response_dict = get_organization_usage200_response_instance.to_dict()
# create an instance of GetOrganizationUsage200Response from a dict
get_organization_usage200_response_from_dict = GetOrganizationUsage200Response.from_dict(get_organization_usage200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


