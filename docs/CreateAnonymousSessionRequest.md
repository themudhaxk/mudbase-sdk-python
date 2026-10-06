# CreateAnonymousSessionRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**project_id** | **str** | Project ID for the anonymous session | [optional] 
**device_id** | **str** | Optional device identifier | [optional] 

## Example

```python
from mudbase.models.create_anonymous_session_request import CreateAnonymousSessionRequest

# TODO update the JSON string below
json = "{}"
# create an instance of CreateAnonymousSessionRequest from a JSON string
create_anonymous_session_request_instance = CreateAnonymousSessionRequest.from_json(json)
# print the JSON string representation of the object
print(CreateAnonymousSessionRequest.to_json())

# convert the object into a dict
create_anonymous_session_request_dict = create_anonymous_session_request_instance.to_dict()
# create an instance of CreateAnonymousSessionRequest from a dict
create_anonymous_session_request_from_dict = CreateAnonymousSessionRequest.from_dict(create_anonymous_session_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


