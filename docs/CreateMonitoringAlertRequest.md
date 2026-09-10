# CreateMonitoringAlertRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** |  | [optional] 
**condition** | **str** |  | [optional] 
**threshold** | **float** |  | [optional] 
**action** | **str** |  | [optional] 
**project_id** | **str** |  | [optional] 

## Example

```python
from mudbase.models.create_monitoring_alert_request import CreateMonitoringAlertRequest

# TODO update the JSON string below
json = "{}"
# create an instance of CreateMonitoringAlertRequest from a JSON string
create_monitoring_alert_request_instance = CreateMonitoringAlertRequest.from_json(json)
# print the JSON string representation of the object
print(CreateMonitoringAlertRequest.to_json())

# convert the object into a dict
create_monitoring_alert_request_dict = create_monitoring_alert_request_instance.to_dict()
# create an instance of CreateMonitoringAlertRequest from a dict
create_monitoring_alert_request_from_dict = CreateMonitoringAlertRequest.from_dict(create_monitoring_alert_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


