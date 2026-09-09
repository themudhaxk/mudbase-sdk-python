# ExportUserData200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**exported_at** | **datetime** |  | [optional] 
**user** | [**User**](User.md) |  | [optional] 
**projects** | **List[Dict[str, object]]** |  | [optional] 
**wallets** | **List[Dict[str, object]]** |  | [optional] 
**transactions** | **List[Dict[str, object]]** |  | [optional] 
**files** | **List[Dict[str, object]]** |  | [optional] 
**integrations** | **List[Dict[str, object]]** |  | [optional] 
**api_keys** | **List[Dict[str, object]]** |  | [optional] 

## Example

```python
from mudbase.models.export_user_data200_response import ExportUserData200Response

# TODO update the JSON string below
json = "{}"
# create an instance of ExportUserData200Response from a JSON string
export_user_data200_response_instance = ExportUserData200Response.from_json(json)
# print the JSON string representation of the object
print(ExportUserData200Response.to_json())

# convert the object into a dict
export_user_data200_response_dict = export_user_data200_response_instance.to_dict()
# create an instance of ExportUserData200Response from a dict
export_user_data200_response_from_dict = ExportUserData200Response.from_dict(export_user_data200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


