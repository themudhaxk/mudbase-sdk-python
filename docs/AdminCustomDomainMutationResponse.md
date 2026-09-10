# AdminCustomDomainMutationResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**success** | **bool** |  | 
**domain** | [**OrgDomainEntryWithDns**](OrgDomainEntryWithDns.md) |  | 

## Example

```python
from mudbase.models.admin_custom_domain_mutation_response import AdminCustomDomainMutationResponse

# TODO update the JSON string below
json = "{}"
# create an instance of AdminCustomDomainMutationResponse from a JSON string
admin_custom_domain_mutation_response_instance = AdminCustomDomainMutationResponse.from_json(json)
# print the JSON string representation of the object
print(AdminCustomDomainMutationResponse.to_json())

# convert the object into a dict
admin_custom_domain_mutation_response_dict = admin_custom_domain_mutation_response_instance.to_dict()
# create an instance of AdminCustomDomainMutationResponse from a dict
admin_custom_domain_mutation_response_from_dict = AdminCustomDomainMutationResponse.from_dict(admin_custom_domain_mutation_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


