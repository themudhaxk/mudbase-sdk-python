# InitiateOrgOAuth400Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**error** | **str** |  | [optional] 
**message** | **str** |  | [optional] 

## Example

```python
from mudbase.models.initiate_org_o_auth400_response import InitiateOrgOAuth400Response

# TODO update the JSON string below
json = "{}"
# create an instance of InitiateOrgOAuth400Response from a JSON string
initiate_org_o_auth400_response_instance = InitiateOrgOAuth400Response.from_json(json)
# print the JSON string representation of the object
print(InitiateOrgOAuth400Response.to_json())

# convert the object into a dict
initiate_org_o_auth400_response_dict = initiate_org_o_auth400_response_instance.to_dict()
# create an instance of InitiateOrgOAuth400Response from a dict
initiate_org_o_auth400_response_from_dict = InitiateOrgOAuth400Response.from_dict(initiate_org_o_auth400_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


