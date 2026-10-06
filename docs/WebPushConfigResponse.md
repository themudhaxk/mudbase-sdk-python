# WebPushConfigResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**success** | **bool** |  | [optional] 
**data** | [**WebPushConfigResponseData**](WebPushConfigResponseData.md) |  | [optional] 

## Example

```python
from mudbase.models.web_push_config_response import WebPushConfigResponse

# TODO update the JSON string below
json = "{}"
# create an instance of WebPushConfigResponse from a JSON string
web_push_config_response_instance = WebPushConfigResponse.from_json(json)
# print the JSON string representation of the object
print(WebPushConfigResponse.to_json())

# convert the object into a dict
web_push_config_response_dict = web_push_config_response_instance.to_dict()
# create an instance of WebPushConfigResponse from a dict
web_push_config_response_from_dict = WebPushConfigResponse.from_dict(web_push_config_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


