# WebPushConfigResponseData


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**enabled** | **bool** | Whether native Web Push is enabled for this project. | [optional] 
**has_keys** | **bool** | Whether a VAPID keypair has been provisioned. | [optional] 
**public_key** | **str** | The VAPID application-server public key clients subscribe with. Null when native Web Push is not enabled.  | [optional] 
**vapid_subject** | **str** | RFC 8292 contact subject (a &#x60;mailto:&#x60; address or &#x60;https&#x60; URL). | [optional] 
**generated_at** | **datetime** | When the current VAPID keypair was generated. | [optional] 

## Example

```python
from mudbase.models.web_push_config_response_data import WebPushConfigResponseData

# TODO update the JSON string below
json = "{}"
# create an instance of WebPushConfigResponseData from a JSON string
web_push_config_response_data_instance = WebPushConfigResponseData.from_json(json)
# print the JSON string representation of the object
print(WebPushConfigResponseData.to_json())

# convert the object into a dict
web_push_config_response_data_dict = web_push_config_response_data_instance.to_dict()
# create an instance of WebPushConfigResponseData from a dict
web_push_config_response_data_from_dict = WebPushConfigResponseData.from_dict(web_push_config_response_data_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


