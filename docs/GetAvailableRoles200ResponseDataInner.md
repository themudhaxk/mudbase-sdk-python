# GetAvailableRoles200ResponseDataInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**slug** | **str** |  | [optional] 
**name** | **str** |  | [optional] 
**description** | **str** |  | [optional] 
**signup_endpoint** | **str** |  | [optional] 
**requires_approval** | **bool** |  | [optional] 
**requires_payment** | **bool** |  | [optional] 
**requires_kyc** | **bool** |  | [optional] 

## Example

```python
from mudbase.models.get_available_roles200_response_data_inner import GetAvailableRoles200ResponseDataInner

# TODO update the JSON string below
json = "{}"
# create an instance of GetAvailableRoles200ResponseDataInner from a JSON string
get_available_roles200_response_data_inner_instance = GetAvailableRoles200ResponseDataInner.from_json(json)
# print the JSON string representation of the object
print(GetAvailableRoles200ResponseDataInner.to_json())

# convert the object into a dict
get_available_roles200_response_data_inner_dict = get_available_roles200_response_data_inner_instance.to_dict()
# create an instance of GetAvailableRoles200ResponseDataInner from a dict
get_available_roles200_response_data_inner_from_dict = GetAvailableRoles200ResponseDataInner.from_dict(get_available_roles200_response_data_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


