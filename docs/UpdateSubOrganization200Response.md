# UpdateSubOrganization200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**message** | **str** |  | [optional] 
**org** | [**Organization**](Organization.md) |  | [optional] 

## Example

```python
from mudbase.models.update_sub_organization200_response import UpdateSubOrganization200Response

# TODO update the JSON string below
json = "{}"
# create an instance of UpdateSubOrganization200Response from a JSON string
update_sub_organization200_response_instance = UpdateSubOrganization200Response.from_json(json)
# print the JSON string representation of the object
print(UpdateSubOrganization200Response.to_json())

# convert the object into a dict
update_sub_organization200_response_dict = update_sub_organization200_response_instance.to_dict()
# create an instance of UpdateSubOrganization200Response from a dict
update_sub_organization200_response_from_dict = UpdateSubOrganization200Response.from_dict(update_sub_organization200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


