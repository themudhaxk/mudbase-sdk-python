# LogSecurityEventRequestDetails


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**user_id** | **str** |  | [optional] 
**resource** | **str** |  | [optional] 
**ip_address** | **str** |  | [optional] 
**user_agent** | **str** |  | [optional] 
**action** | **str** |  | [optional] 
**reason** | **str** |  | [optional] 

## Example

```python
from mudbase.models.log_security_event_request_details import LogSecurityEventRequestDetails

# TODO update the JSON string below
json = "{}"
# create an instance of LogSecurityEventRequestDetails from a JSON string
log_security_event_request_details_instance = LogSecurityEventRequestDetails.from_json(json)
# print the JSON string representation of the object
print(LogSecurityEventRequestDetails.to_json())

# convert the object into a dict
log_security_event_request_details_dict = log_security_event_request_details_instance.to_dict()
# create an instance of LogSecurityEventRequestDetails from a dict
log_security_event_request_details_from_dict = LogSecurityEventRequestDetails.from_dict(log_security_event_request_details_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


