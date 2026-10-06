# GetProjectCaptchaConfig200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**captcha** | [**GetProjectCaptchaConfig200ResponseCaptcha**](GetProjectCaptchaConfig200ResponseCaptcha.md) |  | [optional] 

## Example

```python
from mudbase.models.get_project_captcha_config200_response import GetProjectCaptchaConfig200Response

# TODO update the JSON string below
json = "{}"
# create an instance of GetProjectCaptchaConfig200Response from a JSON string
get_project_captcha_config200_response_instance = GetProjectCaptchaConfig200Response.from_json(json)
# print the JSON string representation of the object
print(GetProjectCaptchaConfig200Response.to_json())

# convert the object into a dict
get_project_captcha_config200_response_dict = get_project_captcha_config200_response_instance.to_dict()
# create an instance of GetProjectCaptchaConfig200Response from a dict
get_project_captcha_config200_response_from_dict = GetProjectCaptchaConfig200Response.from_dict(get_project_captcha_config200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


