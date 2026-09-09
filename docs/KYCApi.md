# mudbase.KYCApi

All URIs are relative to *https://cloud.mudbase.dev*

Method | HTTP request | Description
------------- | ------------- | -------------
[**api_kyc_events_get**](KYCApi.md#api_kyc_events_get) | **GET** /api/kyc/events | List recent compliance webhook deliveries
[**api_kyc_sessions_post**](KYCApi.md#api_kyc_sessions_post) | **POST** /api/kyc/sessions | Start a platform KYC session
[**api_kyc_status_get**](KYCApi.md#api_kyc_status_get) | **GET** /api/kyc/status | Get the organization&#39;s platform KYC status
[**api_kyc_verifications_id_get**](KYCApi.md#api_kyc_verifications_id_get) | **GET** /api/kyc/verifications/{id} | Get a single KYC verification record
[**api_kyc_webhook_config_get**](KYCApi.md#api_kyc_webhook_config_get) | **GET** /api/kyc/webhook-config | Get white-label KYC webhook config
[**api_kyc_webhook_config_put**](KYCApi.md#api_kyc_webhook_config_put) | **PUT** /api/kyc/webhook-config | Set white-label KYC webhook config
[**api_kyc_webhook_config_test_post**](KYCApi.md#api_kyc_webhook_config_test_post) | **POST** /api/kyc/webhook-config/test | Send a signed test event to the configured webhook endpoint
[**api_kyc_workflows_get**](KYCApi.md#api_kyc_workflows_get) | **GET** /api/kyc/workflows | List available verification workflows
[**api_projects_project_id_kyb_sessions_post**](KYCApi.md#api_projects_project_id_kyb_sessions_post) | **POST** /api/projects/{projectId}/kyb/sessions | Start a business verification (KYB) session for one of your business customers


# **api_kyc_events_get**
> api_kyc_events_get(limit=limit)

List recent compliance webhook deliveries

Audit trail of compliance webhook events received for this organization and whether Mudbase forwarded each one to the organization's own endpoint. Owner, admin, and developer roles.

### Example

* Bearer (JWT) Authentication (OrgBearerAuth):

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

# Enter a context with an instance of the API client
with mudbase.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = mudbase.KYCApi(api_client)
    limit = 25 # int | Maximum number of events to return. (optional) (default to 25)

    try:
        # List recent compliance webhook deliveries
        api_instance.api_kyc_events_get(limit=limit)
    except Exception as e:
        print("Exception when calling KYCApi->api_kyc_events_get: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **limit** | **int**| Maximum number of events to return. | [optional] [default to 25]

### Return type

void (empty response body)

### Authorization

[OrgBearerAuth](../README.md#OrgBearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Recent events, newest first |  -  |
**401** | Authentication required |  -  |
**403** | Insufficient role |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **api_kyc_sessions_post**
> api_kyc_sessions_post(api_kyc_sessions_post_request=api_kyc_sessions_post_request)

Start a platform KYC session

Creates a verification session for the caller's organization. Owner/admin only.

### Example

* Bearer (JWT) Authentication (OrgBearerAuth):

```python
import mudbase
from mudbase.models.api_kyc_sessions_post_request import ApiKycSessionsPostRequest
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

# Enter a context with an instance of the API client
with mudbase.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = mudbase.KYCApi(api_client)
    api_kyc_sessions_post_request = mudbase.ApiKycSessionsPostRequest() # ApiKycSessionsPostRequest |  (optional)

    try:
        # Start a platform KYC session
        api_instance.api_kyc_sessions_post(api_kyc_sessions_post_request=api_kyc_sessions_post_request)
    except Exception as e:
        print("Exception when calling KYCApi->api_kyc_sessions_post: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **api_kyc_sessions_post_request** | [**ApiKycSessionsPostRequest**](ApiKycSessionsPostRequest.md)|  | [optional] 

### Return type

void (empty response body)

### Authorization

[OrgBearerAuth](../README.md#OrgBearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Session created (returns the verification session URL and identifiers) |  -  |
**401** | Authentication required |  -  |
**403** | Insufficient role (owner/admin required) |  -  |
**429** | Rate limit exceeded |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **api_kyc_status_get**
> api_kyc_status_get()

Get the organization's platform KYC status

### Example

* Bearer (JWT) Authentication (OrgBearerAuth):

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

# Enter a context with an instance of the API client
with mudbase.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = mudbase.KYCApi(api_client)

    try:
        # Get the organization's platform KYC status
        api_instance.api_kyc_status_get()
    except Exception as e:
        print("Exception when calling KYCApi->api_kyc_status_get: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

void (empty response body)

### Authorization

[OrgBearerAuth](../README.md#OrgBearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Current KYC status for the caller&#39;s organization |  -  |
**401** | Authentication required |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **api_kyc_verifications_id_get**
> api_kyc_verifications_id_get(id)

Get a single KYC verification record

### Example

* Bearer (JWT) Authentication (OrgBearerAuth):

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

# Enter a context with an instance of the API client
with mudbase.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = mudbase.KYCApi(api_client)
    id = 'id_example' # str | Verification record id.

    try:
        # Get a single KYC verification record
        api_instance.api_kyc_verifications_id_get(id)
    except Exception as e:
        print("Exception when calling KYCApi->api_kyc_verifications_id_get: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| Verification record id. | 

### Return type

void (empty response body)

### Authorization

[OrgBearerAuth](../README.md#OrgBearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The verification record |  -  |
**401** | Authentication required |  -  |
**404** | Verification not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **api_kyc_webhook_config_get**
> ApiKycWebhookConfigGet200Response api_kyc_webhook_config_get()

Get white-label KYC webhook config

Returns the destination URL where the organization's own system receives KYC results and whether a signing secret is set. The secret value itself is never returned. Owner/admin only.

### Example

* Bearer (JWT) Authentication (OrgBearerAuth):

```python
import mudbase
from mudbase.models.api_kyc_webhook_config_get200_response import ApiKycWebhookConfigGet200Response
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

# Enter a context with an instance of the API client
with mudbase.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = mudbase.KYCApi(api_client)

    try:
        # Get white-label KYC webhook config
        api_response = api_instance.api_kyc_webhook_config_get()
        print("The response of KYCApi->api_kyc_webhook_config_get:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling KYCApi->api_kyc_webhook_config_get: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

[**ApiKycWebhookConfigGet200Response**](ApiKycWebhookConfigGet200Response.md)

### Authorization

[OrgBearerAuth](../README.md#OrgBearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Current webhook config |  -  |
**401** | Authentication required |  -  |
**403** | Insufficient role (owner/admin required) |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **api_kyc_webhook_config_put**
> ApiKycWebhookConfigPut200Response api_kyc_webhook_config_put(api_kyc_webhook_config_put_request=api_kyc_webhook_config_put_request)

Set white-label KYC webhook config

Updates the destination URL and/or signing secret used to deliver KYC results to the organization's own system. The outbound URL is SSRF-validated. When generateSecret is true a new secret is created and returned once. Owner/admin only.

### Example

* Bearer (JWT) Authentication (OrgBearerAuth):

```python
import mudbase
from mudbase.models.api_kyc_webhook_config_put200_response import ApiKycWebhookConfigPut200Response
from mudbase.models.api_kyc_webhook_config_put_request import ApiKycWebhookConfigPutRequest
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

# Enter a context with an instance of the API client
with mudbase.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = mudbase.KYCApi(api_client)
    api_kyc_webhook_config_put_request = mudbase.ApiKycWebhookConfigPutRequest() # ApiKycWebhookConfigPutRequest |  (optional)

    try:
        # Set white-label KYC webhook config
        api_response = api_instance.api_kyc_webhook_config_put(api_kyc_webhook_config_put_request=api_kyc_webhook_config_put_request)
        print("The response of KYCApi->api_kyc_webhook_config_put:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling KYCApi->api_kyc_webhook_config_put: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **api_kyc_webhook_config_put_request** | [**ApiKycWebhookConfigPutRequest**](ApiKycWebhookConfigPutRequest.md)|  | [optional] 

### Return type

[**ApiKycWebhookConfigPut200Response**](ApiKycWebhookConfigPut200Response.md)

### Authorization

[OrgBearerAuth](../README.md#OrgBearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Updated webhook config (includes webhookSecret only when freshly generated) |  -  |
**400** | Invalid webhookUrl or webhookSecret |  -  |
**401** | Authentication required |  -  |
**403** | Insufficient role (owner/admin required) |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **api_kyc_webhook_config_test_post**
> ApiKycWebhookConfigTestPost200Response api_kyc_webhook_config_test_post()

Send a signed test event to the configured webhook endpoint

Delivers a sample `kyc.test` payload, signed exactly like a real event, so you can confirm your receiver and signature verification work. Ignores your event subscription. Owner/admin only.

### Example

* Bearer (JWT) Authentication (OrgBearerAuth):

```python
import mudbase
from mudbase.models.api_kyc_webhook_config_test_post200_response import ApiKycWebhookConfigTestPost200Response
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

# Enter a context with an instance of the API client
with mudbase.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = mudbase.KYCApi(api_client)

    try:
        # Send a signed test event to the configured webhook endpoint
        api_response = api_instance.api_kyc_webhook_config_test_post()
        print("The response of KYCApi->api_kyc_webhook_config_test_post:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling KYCApi->api_kyc_webhook_config_test_post: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

[**ApiKycWebhookConfigTestPost200Response**](ApiKycWebhookConfigTestPost200Response.md)

### Authorization

[OrgBearerAuth](../README.md#OrgBearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Delivery outcome |  -  |
**400** | No webhook URL or signing secret configured |  -  |
**401** | Authentication required |  -  |
**403** | Insufficient role (owner/admin required) |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **api_kyc_workflows_get**
> ApiKycWorkflowsGet200Response api_kyc_workflows_get()

List available verification workflows

Returns the verification workflows configured on this Mudbase account, split into kyc (individual identity) and kyb (business verification). Used to choose a default workflow in the console instead of pasting a workflow UUID. Owner/admin only.

### Example

* Bearer (JWT) Authentication (OrgBearerAuth):

```python
import mudbase
from mudbase.models.api_kyc_workflows_get200_response import ApiKycWorkflowsGet200Response
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

# Enter a context with an instance of the API client
with mudbase.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = mudbase.KYCApi(api_client)

    try:
        # List available verification workflows
        api_response = api_instance.api_kyc_workflows_get()
        print("The response of KYCApi->api_kyc_workflows_get:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling KYCApi->api_kyc_workflows_get: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

[**ApiKycWorkflowsGet200Response**](ApiKycWorkflowsGet200Response.md)

### Authorization

[OrgBearerAuth](../README.md#OrgBearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Available workflows grouped by product |  -  |
**401** | Authentication required |  -  |
**403** | Insufficient role (owner/admin required) |  -  |
**503** | KYC is not configured on this server |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **api_projects_project_id_kyb_sessions_post**
> api_projects_project_id_kyb_sessions_post(project_id, api_projects_project_id_kyb_sessions_post_request=api_projects_project_id_kyb_sessions_post_request)

Start a business verification (KYB) session for one of your business customers

Creates a KYB session scoped to your project. The workflow is resolved from the request, then the organization's configured default KYB workflow, then the platform default. Results arrive at your configured KYC webhook as `kyb.completed`.

### Example

* Bearer (JWT) Authentication (OrgBearerAuth):

```python
import mudbase
from mudbase.models.api_projects_project_id_kyb_sessions_post_request import ApiProjectsProjectIdKybSessionsPostRequest
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

# Enter a context with an instance of the API client
with mudbase.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = mudbase.KYCApi(api_client)
    project_id = 'project_id_example' # str | 
    api_projects_project_id_kyb_sessions_post_request = mudbase.ApiProjectsProjectIdKybSessionsPostRequest() # ApiProjectsProjectIdKybSessionsPostRequest |  (optional)

    try:
        # Start a business verification (KYB) session for one of your business customers
        api_instance.api_projects_project_id_kyb_sessions_post(project_id, api_projects_project_id_kyb_sessions_post_request=api_projects_project_id_kyb_sessions_post_request)
    except Exception as e:
        print("Exception when calling KYCApi->api_projects_project_id_kyb_sessions_post: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **str**|  | 
 **api_projects_project_id_kyb_sessions_post_request** | [**ApiProjectsProjectIdKybSessionsPostRequest**](ApiProjectsProjectIdKybSessionsPostRequest.md)|  | [optional] 

### Return type

void (empty response body)

### Authorization

[OrgBearerAuth](../README.md#OrgBearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | KYB session created (returns the hosted verification URL) |  -  |
**400** | No KYB workflow configured, or invalid input |  -  |
**401** | Authentication required |  -  |
**503** | KYC is not configured on this server |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

