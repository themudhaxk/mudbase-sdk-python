# UpdateOrganization200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**message** | **str** |  | [optional] 
**org** | [**Organization**](Organization.md) |  | [optional] 

## Example

```python
from mudbase.models.update_organization200_response import UpdateOrganization200Response

# TODO update the JSON string below
json = "{}"
# create an instance of UpdateOrganization200Response from a JSON string
update_organization200_response_instance = UpdateOrganization200Response.from_json(json)
# print the JSON string representation of the object
print(UpdateOrganization200Response.to_json())

# convert the object into a dict
update_organization200_response_dict = update_organization200_response_instance.to_dict()
# create an instance of UpdateOrganization200Response from a dict
update_organization200_response_from_dict = UpdateOrganization200Response.from_dict(update_organization200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


