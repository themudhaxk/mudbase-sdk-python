# EraseUserData409Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**error** | **str** |  | [optional] 
**sole_owned_orgs** | **List[str]** |  | [optional] 

## Example

```python
from mudbase.models.erase_user_data409_response import EraseUserData409Response

# TODO update the JSON string below
json = "{}"
# create an instance of EraseUserData409Response from a JSON string
erase_user_data409_response_instance = EraseUserData409Response.from_json(json)
# print the JSON string representation of the object
print(EraseUserData409Response.to_json())

# convert the object into a dict
erase_user_data409_response_dict = erase_user_data409_response_instance.to_dict()
# create an instance of EraseUserData409Response from a dict
erase_user_data409_response_from_dict = EraseUserData409Response.from_dict(erase_user_data409_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


