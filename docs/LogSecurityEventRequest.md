# LogSecurityEventRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**event_type** | **str** |  | 
**severity** | **str** |  | 
**details** | [**LogSecurityEventRequestDetails**](LogSecurityEventRequestDetails.md) |  | [optional] 

## Example

```python
from mudbase.models.log_security_event_request import LogSecurityEventRequest

# TODO update the JSON string below
json = "{}"
# create an instance of LogSecurityEventRequest from a JSON string
log_security_event_request_instance = LogSecurityEventRequest.from_json(json)
# print the JSON string representation of the object
print(LogSecurityEventRequest.to_json())

# convert the object into a dict
log_security_event_request_dict = log_security_event_request_instance.to_dict()
# create an instance of LogSecurityEventRequest from a dict
log_security_event_request_from_dict = LogSecurityEventRequest.from_dict(log_security_event_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


