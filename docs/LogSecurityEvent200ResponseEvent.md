# LogSecurityEvent200ResponseEvent


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** |  | [optional] 
**event_type** | **str** |  | [optional] 
**severity** | **str** |  | [optional] 
**timestamp** | **datetime** |  | [optional] 

## Example

```python
from mudbase.models.log_security_event200_response_event import LogSecurityEvent200ResponseEvent

# TODO update the JSON string below
json = "{}"
# create an instance of LogSecurityEvent200ResponseEvent from a JSON string
log_security_event200_response_event_instance = LogSecurityEvent200ResponseEvent.from_json(json)
# print the JSON string representation of the object
print(LogSecurityEvent200ResponseEvent.to_json())

# convert the object into a dict
log_security_event200_response_event_dict = log_security_event200_response_event_instance.to_dict()
# create an instance of LogSecurityEvent200ResponseEvent from a dict
log_security_event200_response_event_from_dict = LogSecurityEvent200ResponseEvent.from_dict(log_security_event200_response_event_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


