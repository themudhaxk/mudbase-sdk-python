# ProjectSmsByoPatchRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**enabled** | **bool** |  | [optional] 
**provider** | **str** |  | [optional] 
**default_from** | **str** | Default sender (E.164 for Twilio; Termii/Africa&#39;s Talking may use alphanumeric or approved sender IDs per provider rules). | [optional] 
**config** | **Dict[str, object]** | Provider credentials and options (encrypted at rest). Required keys when enabling BYO: **twilio** — &#x60;accountSid&#x60;, &#x60;authToken&#x60;. Optional &#x60;from&#x60;. **termii** — &#x60;apiKey&#x60;. Optional &#x60;from&#x60;. **africastalking** — &#x60;username&#x60;, &#x60;apiKey&#x60;. Optional &#x60;from&#x60;.  | [optional] 

## Example

```python
from mudbase.models.project_sms_byo_patch_request import ProjectSmsByoPatchRequest

# TODO update the JSON string below
json = "{}"
# create an instance of ProjectSmsByoPatchRequest from a JSON string
project_sms_byo_patch_request_instance = ProjectSmsByoPatchRequest.from_json(json)
# print the JSON string representation of the object
print(ProjectSmsByoPatchRequest.to_json())

# convert the object into a dict
project_sms_byo_patch_request_dict = project_sms_byo_patch_request_instance.to_dict()
# create an instance of ProjectSmsByoPatchRequest from a dict
project_sms_byo_patch_request_from_dict = ProjectSmsByoPatchRequest.from_dict(project_sms_byo_patch_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


