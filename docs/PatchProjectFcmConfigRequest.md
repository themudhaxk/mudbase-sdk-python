# PatchProjectFcmConfigRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**service_account_json** | **object** | Firebase service account JSON (client_email, private_key, etc.) | 
**clear** | **bool** |  | 

## Example

```python
from mudbase.models.patch_project_fcm_config_request import PatchProjectFcmConfigRequest

# TODO update the JSON string below
json = "{}"
# create an instance of PatchProjectFcmConfigRequest from a JSON string
patch_project_fcm_config_request_instance = PatchProjectFcmConfigRequest.from_json(json)
# print the JSON string representation of the object
print(PatchProjectFcmConfigRequest.to_json())

# convert the object into a dict
patch_project_fcm_config_request_dict = patch_project_fcm_config_request_instance.to_dict()
# create an instance of PatchProjectFcmConfigRequest from a dict
patch_project_fcm_config_request_from_dict = PatchProjectFcmConfigRequest.from_dict(patch_project_fcm_config_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


