# CreateOrganization403Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**error** | **str** |  | [optional] 
**code** | **str** |  | [optional] 

## Example

```python
from mudbase.models.create_organization403_response import CreateOrganization403Response

# TODO update the JSON string below
json = "{}"
# create an instance of CreateOrganization403Response from a JSON string
create_organization403_response_instance = CreateOrganization403Response.from_json(json)
# print the JSON string representation of the object
print(CreateOrganization403Response.to_json())

# convert the object into a dict
create_organization403_response_dict = create_organization403_response_instance.to_dict()
# create an instance of CreateOrganization403Response from a dict
create_organization403_response_from_dict = CreateOrganization403Response.from_dict(create_organization403_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


