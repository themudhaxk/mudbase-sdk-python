# SystemStatusResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**success** | **bool** |  | [optional] 
**data** | [**SystemStatusResponseData**](SystemStatusResponseData.md) |  | [optional] 

## Example

```python
from mudbase.models.system_status_response import SystemStatusResponse

# TODO update the JSON string below
json = "{}"
# create an instance of SystemStatusResponse from a JSON string
system_status_response_instance = SystemStatusResponse.from_json(json)
# print the JSON string representation of the object
print(SystemStatusResponse.to_json())

# convert the object into a dict
system_status_response_dict = system_status_response_instance.to_dict()
# create an instance of SystemStatusResponse from a dict
system_status_response_from_dict = SystemStatusResponse.from_dict(system_status_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


