# PatchProjectFcmConfigRequestOneOf


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**service_account_json** | **object** | Firebase service account JSON (client_email, private_key, etc.) | 

## Example

```python
from mudbase.models.patch_project_fcm_config_request_one_of import PatchProjectFcmConfigRequestOneOf

# TODO update the JSON string below
json = "{}"
# create an instance of PatchProjectFcmConfigRequestOneOf from a JSON string
patch_project_fcm_config_request_one_of_instance = PatchProjectFcmConfigRequestOneOf.from_json(json)
# print the JSON string representation of the object
print(PatchProjectFcmConfigRequestOneOf.to_json())

# convert the object into a dict
patch_project_fcm_config_request_one_of_dict = patch_project_fcm_config_request_one_of_instance.to_dict()
# create an instance of PatchProjectFcmConfigRequestOneOf from a dict
patch_project_fcm_config_request_one_of_from_dict = PatchProjectFcmConfigRequestOneOf.from_dict(patch_project_fcm_config_request_one_of_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


