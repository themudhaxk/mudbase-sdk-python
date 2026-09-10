# GetProjectCaptchaConfig200ResponseCaptcha


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**enabled** | **bool** | Whether CAPTCHA is enabled for this project | [optional] 
**version** | **str** | reCAPTCHA version (v2 or v3) | [optional] 
**site_key** | **str** | Public site key for frontend integration | [optional] 
**min_score** | **float** | Minimum score threshold for reCAPTCHA v3 | [optional] 

## Example

```python
from mudbase.models.get_project_captcha_config200_response_captcha import GetProjectCaptchaConfig200ResponseCaptcha

# TODO update the JSON string below
json = "{}"
# create an instance of GetProjectCaptchaConfig200ResponseCaptcha from a JSON string
get_project_captcha_config200_response_captcha_instance = GetProjectCaptchaConfig200ResponseCaptcha.from_json(json)
# print the JSON string representation of the object
print(GetProjectCaptchaConfig200ResponseCaptcha.to_json())

# convert the object into a dict
get_project_captcha_config200_response_captcha_dict = get_project_captcha_config200_response_captcha_instance.to_dict()
# create an instance of GetProjectCaptchaConfig200ResponseCaptcha from a dict
get_project_captcha_config200_response_captcha_from_dict = GetProjectCaptchaConfig200ResponseCaptcha.from_dict(get_project_captcha_config200_response_captcha_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


