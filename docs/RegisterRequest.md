# RegisterRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**email** | **str** |  | 
**password** | **str** |  | 
**first_name** | **str** |  | 
**last_name** | **str** |  | 
**org_name** | **str** |  | [optional] 
**agreed_to_terms** | **bool** | Must be &#x60;true&#x60; - the server rejects the request otherwise. Required to stop a direct API call from creating an account without accepting the Terms of Service and Privacy Policy. | 
**captcha** | **str** | Google reCAPTCHA v3 response token, required only when the platform&#39;s anti-bot CAPTCHA gate is enabled. A missing token then gets a 400 with &#x60;captchaRequired: true&#x60; and a &#x60;siteKey&#x60;. Solving this needs a real browser, so this endpoint backs the web console&#39;s own signup form (&#x60;https://www.mudbase.dev/console/register&#x60;) and is not meant for scripted/server-to-server account creation. To integrate: create your Mudbase account once through the console, then use the API key from Settings -&gt; API Keys for everything else - collections, documents, storage, and the rest of the API are all fully scriptable from there. | [optional] 

## Example

```python
from mudbase.models.register_request import RegisterRequest

# TODO update the JSON string below
json = "{}"
# create an instance of RegisterRequest from a JSON string
register_request_instance = RegisterRequest.from_json(json)
# print the JSON string representation of the object
print(RegisterRequest.to_json())

# convert the object into a dict
register_request_dict = register_request_instance.to_dict()
# create an instance of RegisterRequest from a dict
register_request_from_dict = RegisterRequest.from_dict(register_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


