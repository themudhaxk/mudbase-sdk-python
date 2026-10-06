# EraseUserData200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**success** | **bool** |  | [optional] 
**message** | **str** |  | [optional] 
**data** | [**EraseUserData200ResponseData**](EraseUserData200ResponseData.md) |  | [optional] 

## Example

```python
from mudbase.models.erase_user_data200_response import EraseUserData200Response

# TODO update the JSON string below
json = "{}"
# create an instance of EraseUserData200Response from a JSON string
erase_user_data200_response_instance = EraseUserData200Response.from_json(json)
# print the JSON string representation of the object
print(EraseUserData200Response.to_json())

# convert the object into a dict
erase_user_data200_response_dict = erase_user_data200_response_instance.to_dict()
# create an instance of EraseUserData200Response from a dict
erase_user_data200_response_from_dict = EraseUserData200Response.from_dict(erase_user_data200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


