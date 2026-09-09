# SMSRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**to** | **str** |  | 
**message** | **str** |  | 
**var_from** | **str** |  | [optional] 

## Example

```python
from mudbase.models.sms_request import SMSRequest

# TODO update the JSON string below
json = "{}"
# create an instance of SMSRequest from a JSON string
sms_request_instance = SMSRequest.from_json(json)
# print the JSON string representation of the object
print(SMSRequest.to_json())

# convert the object into a dict
sms_request_dict = sms_request_instance.to_dict()
# create an instance of SMSRequest from a dict
sms_request_from_dict = SMSRequest.from_dict(sms_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


