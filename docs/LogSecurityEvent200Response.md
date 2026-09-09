# LogSecurityEvent200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**message** | **str** |  | [optional] 
**event** | [**LogSecurityEvent200ResponseEvent**](LogSecurityEvent200ResponseEvent.md) |  | [optional] 

## Example

```python
from mudbase.models.log_security_event200_response import LogSecurityEvent200Response

# TODO update the JSON string below
json = "{}"
# create an instance of LogSecurityEvent200Response from a JSON string
log_security_event200_response_instance = LogSecurityEvent200Response.from_json(json)
# print the JSON string representation of the object
print(LogSecurityEvent200Response.to_json())

# convert the object into a dict
log_security_event200_response_dict = log_security_event200_response_instance.to_dict()
# create an instance of LogSecurityEvent200Response from a dict
log_security_event200_response_from_dict = LogSecurityEvent200Response.from_dict(log_security_event200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


