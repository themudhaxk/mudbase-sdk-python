# mudbase.EmailApi

All URIs are relative to *https://cloud.mudbase.dev*

Method | HTTP request | Description
------------- | ------------- | -------------
[**enqueue_project_email**](EmailApi.md#enqueue_project_email) | **POST** /api/projects/{projectId}/email/send | Enqueue project email (worker delivery)
[**get_project_email_analytics**](EmailApi.md#get_project_email_analytics) | **GET** /api/projects/{projectId}/analytics/email | Email analytics for a project
[**get_project_email_smtp**](EmailApi.md#get_project_email_smtp) | **GET** /api/projects/{projectId}/email/smtp | Get project SMTP settings (masked)
[**get_project_email_template**](EmailApi.md#get_project_email_template) | **GET** /api/projects/{projectId}/email/templates/{name} | Get one email template (effective content)
[**list_project_email_templates**](EmailApi.md#list_project_email_templates) | **GET** /api/projects/{projectId}/email/templates | List email templates (full catalog for the project)
[**patch_project_email_smtp**](EmailApi.md#patch_project_email_smtp) | **PATCH** /api/projects/{projectId}/email/smtp | Update project SMTP relay (BYO)
[**preview_project_email_template**](EmailApi.md#preview_project_email_template) | **POST** /api/projects/{projectId}/email/templates/{name}/preview | Render template preview (sanitized HTML, no send)
[**restore_default_project_email_template**](EmailApi.md#restore_default_project_email_template) | **POST** /api/projects/{projectId}/email/templates/{name}/restore-default | Restore from platform global default or remove project override
[**test_project_email_smtp**](EmailApi.md#test_project_email_smtp) | **POST** /api/projects/{projectId}/email/smtp/test | Verify SMTP and send a test message
[**upsert_project_email_template**](EmailApi.md#upsert_project_email_template) | **PUT** /api/projects/{projectId}/email/templates/{name} | Upsert project email template (HTML sanitized; variables must cover {{placeholders}})
[**verify_project_email_smtp_domain**](EmailApi.md#verify_project_email_smtp_domain) | **POST** /api/projects/{projectId}/email/smtp/verify-domain | Check DNS (MX + SPF) for sending domain


# **enqueue_project_email**
> EnqueueProjectEmail202Response enqueue_project_email(project_id, project_email_send_request)

Enqueue project email (worker delivery)

Queues a transactional email for sending through the email worker and configured provider (platform or per-project SMTP).
Provide either `template` (with `data`) or both `subject` and `html`. Returns **202** with `jobId` when accepted.


### Example

* Bearer (JWT) Authentication (OrgBearerAuth):
* Api Key Authentication (ApiKeyAuth):
* Bearer (JWT) Authentication (ProjectBearerAuth):

```python
import mudbase
from mudbase.models.enqueue_project_email202_response import EnqueueProjectEmail202Response
from mudbase.models.project_email_send_request import ProjectEmailSendRequest
from mudbase.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://cloud.mudbase.dev
# See configuration.py for a list of all supported configuration parameters.
configuration = mudbase.Configuration(
    host = "https://cloud.mudbase.dev"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure Bearer authorization (JWT): OrgBearerAuth
configuration = mudbase.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Configure API key authorization: ApiKeyAuth
configuration.api_key['ApiKeyAuth'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['ApiKeyAuth'] = 'Bearer'

# Configure Bearer authorization (JWT): ProjectBearerAuth
configuration = mudbase.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with mudbase.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = mudbase.EmailApi(api_client)
    project_id = 'project_id_example' # str | 
    project_email_send_request = {"template":"magicLink","to":"user@example.com","data":{"userName":"Alex","magicLinkUrl":"https://app.example.com/auth/verify?token=abc","expiresIn":"15 minutes"},"idempotencyKey":"proj123:magicLink:user@example.com"} # ProjectEmailSendRequest | 

    try:
        # Enqueue project email (worker delivery)
        api_response = api_instance.enqueue_project_email(project_id, project_email_send_request)
        print("The response of EmailApi->enqueue_project_email:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling EmailApi->enqueue_project_email: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **str**|  | 
 **project_email_send_request** | [**ProjectEmailSendRequest**](ProjectEmailSendRequest.md)|  | 

### Return type

[**EnqueueProjectEmail202Response**](EnqueueProjectEmail202Response.md)

### Authorization

[OrgBearerAuth](../README.md#OrgBearerAuth), [ApiKeyAuth](../README.md#ApiKeyAuth), [ProjectBearerAuth](../README.md#ProjectBearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**202** | Job accepted |  -  |
**400** | Bad request |  -  |
**503** | Email queue unavailable |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_project_email_analytics**
> GetProjectEmailAnalytics200Response get_project_email_analytics(project_id, var_from=var_from, to=to)

Email analytics for a project

Aggregated email log stats for the project. Optional `from` and `to` query params filter by date range (ISO 8601).


### Example

* Bearer (JWT) Authentication (OrgBearerAuth):
* Api Key Authentication (ApiKeyAuth):
* Bearer (JWT) Authentication (ProjectBearerAuth):

```python
import mudbase
from mudbase.models.get_project_email_analytics200_response import GetProjectEmailAnalytics200Response
from mudbase.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://cloud.mudbase.dev
# See configuration.py for a list of all supported configuration parameters.
configuration = mudbase.Configuration(
    host = "https://cloud.mudbase.dev"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure Bearer authorization (JWT): OrgBearerAuth
configuration = mudbase.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Configure API key authorization: ApiKeyAuth
configuration.api_key['ApiKeyAuth'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['ApiKeyAuth'] = 'Bearer'

# Configure Bearer authorization (JWT): ProjectBearerAuth
configuration = mudbase.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with mudbase.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = mudbase.EmailApi(api_client)
    project_id = 'project_id_example' # str | 
    var_from = '2013-10-20T19:20:30+01:00' # datetime |  (optional)
    to = '2013-10-20T19:20:30+01:00' # datetime |  (optional)

    try:
        # Email analytics for a project
        api_response = api_instance.get_project_email_analytics(project_id, var_from=var_from, to=to)
        print("The response of EmailApi->get_project_email_analytics:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling EmailApi->get_project_email_analytics: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **str**|  | 
 **var_from** | **datetime**|  | [optional] 
 **to** | **datetime**|  | [optional] 

### Return type

[**GetProjectEmailAnalytics200Response**](GetProjectEmailAnalytics200Response.md)

### Authorization

[OrgBearerAuth](../README.md#OrgBearerAuth), [ApiKeyAuth](../README.md#ApiKeyAuth), [ProjectBearerAuth](../README.md#ProjectBearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Analytics payload |  -  |
**401** | Authentication required |  -  |
**403** | Access denied |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_project_email_smtp**
> GetProjectEmailSmtp200Response get_project_email_smtp(project_id)

Get project SMTP settings (masked)

### Example

* Bearer (JWT) Authentication (OrgBearerAuth):
* Api Key Authentication (ApiKeyAuth):
* Bearer (JWT) Authentication (ProjectBearerAuth):

```python
import mudbase
from mudbase.models.get_project_email_smtp200_response import GetProjectEmailSmtp200Response
from mudbase.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://cloud.mudbase.dev
# See configuration.py for a list of all supported configuration parameters.
configuration = mudbase.Configuration(
    host = "https://cloud.mudbase.dev"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure Bearer authorization (JWT): OrgBearerAuth
configuration = mudbase.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Configure API key authorization: ApiKeyAuth
configuration.api_key['ApiKeyAuth'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['ApiKeyAuth'] = 'Bearer'

# Configure Bearer authorization (JWT): ProjectBearerAuth
configuration = mudbase.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with mudbase.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = mudbase.EmailApi(api_client)
    project_id = 'project_id_example' # str | 

    try:
        # Get project SMTP settings (masked)
        api_response = api_instance.get_project_email_smtp(project_id)
        print("The response of EmailApi->get_project_email_smtp:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling EmailApi->get_project_email_smtp: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **str**|  | 

### Return type

[**GetProjectEmailSmtp200Response**](GetProjectEmailSmtp200Response.md)

### Authorization

[OrgBearerAuth](../README.md#OrgBearerAuth), [ApiKeyAuth](../README.md#ApiKeyAuth), [ProjectBearerAuth](../README.md#ProjectBearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | SMTP configuration without secrets |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_project_email_template**
> GetProjectEmailTemplate200Response get_project_email_template(project_id, name)

Get one email template (effective content)

Returns the template body that would be used when sending: project override if present, else global default,
else built-in fallback. **`isProjectOverride`** is true only when this project has a stored row; **`effectiveSource`**
is `project`, `global`, or `builtin`.


### Example

* Bearer (JWT) Authentication (OrgBearerAuth):
* Api Key Authentication (ApiKeyAuth):
* Bearer (JWT) Authentication (ProjectBearerAuth):

```python
import mudbase
from mudbase.models.get_project_email_template200_response import GetProjectEmailTemplate200Response
from mudbase.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://cloud.mudbase.dev
# See configuration.py for a list of all supported configuration parameters.
configuration = mudbase.Configuration(
    host = "https://cloud.mudbase.dev"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure Bearer authorization (JWT): OrgBearerAuth
configuration = mudbase.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Configure API key authorization: ApiKeyAuth
configuration.api_key['ApiKeyAuth'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['ApiKeyAuth'] = 'Bearer'

# Configure Bearer authorization (JWT): ProjectBearerAuth
configuration = mudbase.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with mudbase.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = mudbase.EmailApi(api_client)
    project_id = 'project_id_example' # str | 
    name = 'name_example' # str | 

    try:
        # Get one email template (effective content)
        api_response = api_instance.get_project_email_template(project_id, name)
        print("The response of EmailApi->get_project_email_template:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling EmailApi->get_project_email_template: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **str**|  | 
 **name** | **str**|  | 

### Return type

[**GetProjectEmailTemplate200Response**](GetProjectEmailTemplate200Response.md)

### Authorization

[OrgBearerAuth](../README.md#OrgBearerAuth), [ApiKeyAuth](../README.md#ApiKeyAuth), [ProjectBearerAuth](../README.md#ProjectBearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Template document (resolved for send) |  -  |
**404** | Resource not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_project_email_templates**
> ListProjectEmailTemplates200Response list_project_email_templates(project_id)

List email templates (full catalog for the project)

Returns every template name the worker can resolve for this project: **built-in** defaults, **global** platform
rows (`project: null` in DB), and **project** overrides. Use **`isCustomized`** to see if this project has its
own stored copy; **`effectiveSource`** shows which layer would be used at send time (`project` wins over `global` over `builtin`).


### Example

* Bearer (JWT) Authentication (OrgBearerAuth):
* Api Key Authentication (ApiKeyAuth):
* Bearer (JWT) Authentication (ProjectBearerAuth):

```python
import mudbase
from mudbase.models.list_project_email_templates200_response import ListProjectEmailTemplates200Response
from mudbase.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://cloud.mudbase.dev
# See configuration.py for a list of all supported configuration parameters.
configuration = mudbase.Configuration(
    host = "https://cloud.mudbase.dev"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure Bearer authorization (JWT): OrgBearerAuth
configuration = mudbase.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Configure API key authorization: ApiKeyAuth
configuration.api_key['ApiKeyAuth'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['ApiKeyAuth'] = 'Bearer'

# Configure Bearer authorization (JWT): ProjectBearerAuth
configuration = mudbase.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with mudbase.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = mudbase.EmailApi(api_client)
    project_id = 'project_id_example' # str | 

    try:
        # List email templates (full catalog for the project)
        api_response = api_instance.list_project_email_templates(project_id)
        print("The response of EmailApi->list_project_email_templates:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling EmailApi->list_project_email_templates: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **str**|  | 

### Return type

[**ListProjectEmailTemplates200Response**](ListProjectEmailTemplates200Response.md)

### Authorization

[OrgBearerAuth](../README.md#OrgBearerAuth), [ApiKeyAuth](../README.md#ApiKeyAuth), [ProjectBearerAuth](../README.md#ProjectBearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Template catalog with customization flags |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **patch_project_email_smtp**
> GetProjectEmailSmtp200Response patch_project_email_smtp(project_id, project_smtp_patch_request)

Update project SMTP relay (BYO)

Set `authPass` in the body to store an encrypted password (never returned on GET). Validates host/user when enabling.


### Example

* Bearer (JWT) Authentication (OrgBearerAuth):
* Api Key Authentication (ApiKeyAuth):
* Bearer (JWT) Authentication (ProjectBearerAuth):

```python
import mudbase
from mudbase.models.get_project_email_smtp200_response import GetProjectEmailSmtp200Response
from mudbase.models.project_smtp_patch_request import ProjectSmtpPatchRequest
from mudbase.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://cloud.mudbase.dev
# See configuration.py for a list of all supported configuration parameters.
configuration = mudbase.Configuration(
    host = "https://cloud.mudbase.dev"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure Bearer authorization (JWT): OrgBearerAuth
configuration = mudbase.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Configure API key authorization: ApiKeyAuth
configuration.api_key['ApiKeyAuth'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['ApiKeyAuth'] = 'Bearer'

# Configure Bearer authorization (JWT): ProjectBearerAuth
configuration = mudbase.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with mudbase.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = mudbase.EmailApi(api_client)
    project_id = 'project_id_example' # str | 
    project_smtp_patch_request = {"enabled":true,"host":"smtp.sendgrid.net","port":587,"secure":false,"authUser":"apikey","authPass":"SG.xxxx","fromName":"Acme App","fromEmail":"noreply@mail.example.com"} # ProjectSmtpPatchRequest | 

    try:
        # Update project SMTP relay (BYO)
        api_response = api_instance.patch_project_email_smtp(project_id, project_smtp_patch_request)
        print("The response of EmailApi->patch_project_email_smtp:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling EmailApi->patch_project_email_smtp: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **str**|  | 
 **project_smtp_patch_request** | [**ProjectSmtpPatchRequest**](ProjectSmtpPatchRequest.md)|  | 

### Return type

[**GetProjectEmailSmtp200Response**](GetProjectEmailSmtp200Response.md)

### Authorization

[OrgBearerAuth](../README.md#OrgBearerAuth), [ApiKeyAuth](../README.md#ApiKeyAuth), [ProjectBearerAuth](../README.md#ProjectBearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Updated settings (masked) |  -  |
**400** | Bad request |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **preview_project_email_template**
> preview_project_email_template(project_id, name, preview_project_email_template_request=preview_project_email_template_request)

Render template preview (sanitized HTML, no send)

Body **`sampleData`** is merged with layout defaults; keys should match `{{placeholders}}` in the template (see **Email** tag for the catalog).


### Example

* Bearer (JWT) Authentication (OrgBearerAuth):
* Api Key Authentication (ApiKeyAuth):
* Bearer (JWT) Authentication (ProjectBearerAuth):

```python
import mudbase
from mudbase.models.preview_project_email_template_request import PreviewProjectEmailTemplateRequest
from mudbase.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://cloud.mudbase.dev
# See configuration.py for a list of all supported configuration parameters.
configuration = mudbase.Configuration(
    host = "https://cloud.mudbase.dev"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure Bearer authorization (JWT): OrgBearerAuth
configuration = mudbase.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Configure API key authorization: ApiKeyAuth
configuration.api_key['ApiKeyAuth'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['ApiKeyAuth'] = 'Bearer'

# Configure Bearer authorization (JWT): ProjectBearerAuth
configuration = mudbase.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with mudbase.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = mudbase.EmailApi(api_client)
    project_id = 'project_id_example' # str | 
    name = 'name_example' # str | 
    preview_project_email_template_request = {"sampleData":{}} # PreviewProjectEmailTemplateRequest |  (optional)

    try:
        # Render template preview (sanitized HTML, no send)
        api_instance.preview_project_email_template(project_id, name, preview_project_email_template_request=preview_project_email_template_request)
    except Exception as e:
        print("Exception when calling EmailApi->preview_project_email_template: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **str**|  | 
 **name** | **str**|  | 
 **preview_project_email_template_request** | [**PreviewProjectEmailTemplateRequest**](PreviewProjectEmailTemplateRequest.md)|  | [optional] 

### Return type

void (empty response body)

### Authorization

[OrgBearerAuth](../README.md#OrgBearerAuth), [ApiKeyAuth](../README.md#ApiKeyAuth), [ProjectBearerAuth](../README.md#ProjectBearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Rendered subject and HTML |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **restore_default_project_email_template**
> restore_default_project_email_template(project_id, name)

Restore from platform global default or remove project override

### Example

* Bearer (JWT) Authentication (OrgBearerAuth):
* Api Key Authentication (ApiKeyAuth):
* Bearer (JWT) Authentication (ProjectBearerAuth):

```python
import mudbase
from mudbase.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://cloud.mudbase.dev
# See configuration.py for a list of all supported configuration parameters.
configuration = mudbase.Configuration(
    host = "https://cloud.mudbase.dev"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure Bearer authorization (JWT): OrgBearerAuth
configuration = mudbase.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Configure API key authorization: ApiKeyAuth
configuration.api_key['ApiKeyAuth'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['ApiKeyAuth'] = 'Bearer'

# Configure Bearer authorization (JWT): ProjectBearerAuth
configuration = mudbase.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with mudbase.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = mudbase.EmailApi(api_client)
    project_id = 'project_id_example' # str | 
    name = 'name_example' # str | 

    try:
        # Restore from platform global default or remove project override
        api_instance.restore_default_project_email_template(project_id, name)
    except Exception as e:
        print("Exception when calling EmailApi->restore_default_project_email_template: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **str**|  | 
 **name** | **str**|  | 

### Return type

void (empty response body)

### Authorization

[OrgBearerAuth](../README.md#OrgBearerAuth), [ApiKeyAuth](../README.md#ApiKeyAuth), [ProjectBearerAuth](../README.md#ProjectBearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Restored or deleted override |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **test_project_email_smtp**
> DeleteFunction200Response test_project_email_smtp(project_id, project_smtp_test_request)

Verify SMTP and send a test message

Rate-limited. With `useSaved: true` (default), uses stored credentials; otherwise pass `host`, `authUser`, `authPass`, etc.


### Example

* Bearer (JWT) Authentication (OrgBearerAuth):
* Api Key Authentication (ApiKeyAuth):
* Bearer (JWT) Authentication (ProjectBearerAuth):

```python
import mudbase
from mudbase.models.delete_function200_response import DeleteFunction200Response
from mudbase.models.project_smtp_test_request import ProjectSmtpTestRequest
from mudbase.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://cloud.mudbase.dev
# See configuration.py for a list of all supported configuration parameters.
configuration = mudbase.Configuration(
    host = "https://cloud.mudbase.dev"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure Bearer authorization (JWT): OrgBearerAuth
configuration = mudbase.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Configure API key authorization: ApiKeyAuth
configuration.api_key['ApiKeyAuth'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['ApiKeyAuth'] = 'Bearer'

# Configure Bearer authorization (JWT): ProjectBearerAuth
configuration = mudbase.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with mudbase.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = mudbase.EmailApi(api_client)
    project_id = 'project_id_example' # str | 
    project_smtp_test_request = {"to":"ops@example.com","useSaved":true} # ProjectSmtpTestRequest | 

    try:
        # Verify SMTP and send a test message
        api_response = api_instance.test_project_email_smtp(project_id, project_smtp_test_request)
        print("The response of EmailApi->test_project_email_smtp:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling EmailApi->test_project_email_smtp: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **str**|  | 
 **project_smtp_test_request** | [**ProjectSmtpTestRequest**](ProjectSmtpTestRequest.md)|  | 

### Return type

[**DeleteFunction200Response**](DeleteFunction200Response.md)

### Authorization

[OrgBearerAuth](../README.md#OrgBearerAuth), [ApiKeyAuth](../README.md#ApiKeyAuth), [ProjectBearerAuth](../README.md#ProjectBearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | SMTP verified and test mail sent |  -  |
**400** | Bad request |  -  |
**429** | Rate limit exceeded |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **upsert_project_email_template**
> upsert_project_email_template(project_id, name, upsert_project_email_template_request)

Upsert project email template (HTML sanitized; variables must cover {{placeholders}})

Saves a **project override** for `name`. HTML is sanitized. **`variables`** must list every `{{token}}` used in `subject`, `htmlBody`, and `textBody` (see **Email** tag description for the full placeholder catalog).


### Example

* Bearer (JWT) Authentication (OrgBearerAuth):
* Api Key Authentication (ApiKeyAuth):
* Bearer (JWT) Authentication (ProjectBearerAuth):

```python
import mudbase
from mudbase.models.upsert_project_email_template_request import UpsertProjectEmailTemplateRequest
from mudbase.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://cloud.mudbase.dev
# See configuration.py for a list of all supported configuration parameters.
configuration = mudbase.Configuration(
    host = "https://cloud.mudbase.dev"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure Bearer authorization (JWT): OrgBearerAuth
configuration = mudbase.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Configure API key authorization: ApiKeyAuth
configuration.api_key['ApiKeyAuth'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['ApiKeyAuth'] = 'Bearer'

# Configure Bearer authorization (JWT): ProjectBearerAuth
configuration = mudbase.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with mudbase.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = mudbase.EmailApi(api_client)
    project_id = 'project_id_example' # str | 
    name = 'name_example' # str | 
    upsert_project_email_template_request = {"subject":"subject_example","htmlBody":"htmlBody_example"} # UpsertProjectEmailTemplateRequest | 

    try:
        # Upsert project email template (HTML sanitized; variables must cover {{placeholders}})
        api_instance.upsert_project_email_template(project_id, name, upsert_project_email_template_request)
    except Exception as e:
        print("Exception when calling EmailApi->upsert_project_email_template: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **str**|  | 
 **name** | **str**|  | 
 **upsert_project_email_template_request** | [**UpsertProjectEmailTemplateRequest**](UpsertProjectEmailTemplateRequest.md)|  | 

### Return type

void (empty response body)

### Authorization

[OrgBearerAuth](../README.md#OrgBearerAuth), [ApiKeyAuth](../README.md#ApiKeyAuth), [ProjectBearerAuth](../README.md#ProjectBearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Saved template |  -  |
**400** | Bad request |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **verify_project_email_smtp_domain**
> verify_project_email_smtp_domain(project_id, verify_project_email_smtp_domain_request=verify_project_email_smtp_domain_request)

Check DNS (MX + SPF) for sending domain

Resolves the domain from `domain`, `fromEmail`, or saved `emailSmtp.fromEmail`. Returns whether MX and SPF TXT exist.
With `persist: true` and checks passed, sets `emailSmtp.domainVerifiedAt`.


### Example

* Bearer (JWT) Authentication (OrgBearerAuth):
* Api Key Authentication (ApiKeyAuth):
* Bearer (JWT) Authentication (ProjectBearerAuth):

```python
import mudbase
from mudbase.models.verify_project_email_smtp_domain_request import VerifyProjectEmailSmtpDomainRequest
from mudbase.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://cloud.mudbase.dev
# See configuration.py for a list of all supported configuration parameters.
configuration = mudbase.Configuration(
    host = "https://cloud.mudbase.dev"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure Bearer authorization (JWT): OrgBearerAuth
configuration = mudbase.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Configure API key authorization: ApiKeyAuth
configuration.api_key['ApiKeyAuth'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['ApiKeyAuth'] = 'Bearer'

# Configure Bearer authorization (JWT): ProjectBearerAuth
configuration = mudbase.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with mudbase.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = mudbase.EmailApi(api_client)
    project_id = 'project_id_example' # str | 
    verify_project_email_smtp_domain_request = {"domain":"domain_example","fromEmail":"fromEmail_example","persist":true} # VerifyProjectEmailSmtpDomainRequest |  (optional)

    try:
        # Check DNS (MX + SPF) for sending domain
        api_instance.verify_project_email_smtp_domain(project_id, verify_project_email_smtp_domain_request=verify_project_email_smtp_domain_request)
    except Exception as e:
        print("Exception when calling EmailApi->verify_project_email_smtp_domain: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **str**|  | 
 **verify_project_email_smtp_domain_request** | [**VerifyProjectEmailSmtpDomainRequest**](VerifyProjectEmailSmtpDomainRequest.md)|  | [optional] 

### Return type

void (empty response body)

### Authorization

[OrgBearerAuth](../README.md#OrgBearerAuth), [ApiKeyAuth](../README.md#ApiKeyAuth), [ProjectBearerAuth](../README.md#ProjectBearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | DNS check result |  -  |
**400** | Bad request |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

