# UpdateCollectionPermissionsRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**actions** | **List[str]** |  | [optional] 
**conditions** | **object** |  | [optional] 
**data_scope** | **str** | &#x60;all&#x60; &#x3D; no automatic row-owner filter. &#x60;own&#x60; &#x3D; only documents where the owner field matches the authenticated app user. | [optional] 
**owner_field** | **str** | Optional override for the document field when dataScope is &#x60;own&#x60; (default &#x60;settings.dataOwnerField&#x60;, usually &#x60;createdBy&#x60;). | [optional] 

## Example

```python
from mudbase.models.update_collection_permissions_request import UpdateCollectionPermissionsRequest

# TODO update the JSON string below
json = "{}"
# create an instance of UpdateCollectionPermissionsRequest from a JSON string
update_collection_permissions_request_instance = UpdateCollectionPermissionsRequest.from_json(json)
# print the JSON string representation of the object
print(UpdateCollectionPermissionsRequest.to_json())

# convert the object into a dict
update_collection_permissions_request_dict = update_collection_permissions_request_instance.to_dict()
# create an instance of UpdateCollectionPermissionsRequest from a dict
update_collection_permissions_request_from_dict = UpdateCollectionPermissionsRequest.from_dict(update_collection_permissions_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


