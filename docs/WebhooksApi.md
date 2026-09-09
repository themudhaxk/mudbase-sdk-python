# mudbase.WebhooksApi

All URIs are relative to *https://cloud.mudbase.dev*

Method | HTTP request | Description
------------- | ------------- | -------------
[**configure_webhook**](WebhooksApi.md#configure_webhook) | **PUT** /api/webhooks/projects/{projectId}/config | Create or update project webhook
[**get_webhook_config**](WebhooksApi.md#get_webhook_config) | **GET** /api/webhooks/projects/{projectId}/config | Get project webhook configuration
[**get_webhook_stats**](WebhooksApi.md#get_webhook_stats) | **GET** /api/webhooks/stats | Get webhook delivery statistics
[**list_project_webhook_logs**](WebhooksApi.md#list_project_webhook_logs) | **GET** /api/webhooks/projects/{projectId} | List webhook delivery logs (project)
[**list_webhooks**](WebhooksApi.md#list_webhooks) | **GET** /api/webhooks | List webhook delivery logs (organization)
[**retry_webhook**](WebhooksApi.md#retry_webhook) | **POST** /api/webhooks/retry/{webhookId} | Retry a failed webhook delivery
[**test_webhook_transformation**](WebhooksApi.md#test_webhook_transformation) | **POST** /api/webhooks/projects/{projectId}/test-transformation | Test webhook transformation
[**trigger_webhook**](WebhooksApi.md#trigger_webhook) | **POST** /api/webhooks/trigger | Manually trigger an outbound webhook


# **configure_webhook**
> ConfigureWebhook200Response configure_webhook(project_id, configure_webhook_request=configure_webhook_request)

Create or update project webhook

Set or update the project webhook URL and options. This is how you **add** or **create** a webhook for a project:
provide **webhookUrl** to enable delivery; omit or set to null to disable. Optionally set **webhookSecret**,
**webhookEvents**, **webhookVersion**, and **transformations**. Plan limits (webhooks per project) apply when adding a new URL.
Requires ProjectBearerAuth (JWT) or ApiKeyAuth (X-API-Key) with project update access.


### Example

* Bearer (JWT) Authentication (OrgBearerAuth):
* Api Key Authentication (ApiKeyAuth):
* Bearer (JWT) Authentication (ProjectBearerAuth):

```python
import mudbase
from mudbase.models.configure_webhook200_response import ConfigureWebhook200Response
from mudbase.models.configure_webhook_request import ConfigureWebhookRequest
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
    api_instance = mudbase.WebhooksApi(api_client)
    project_id = 'project_id_example' # str | 
    configure_webhook_request = {"webhookUrl":"https://your-app.com/webhooks/mudbase","webhookSecret":"your-secret","webhookEvents":["collection.insert","collection.update","collection.delete"],"webhookVersion":"1.0","transformations":[]} # ConfigureWebhookRequest |  (optional)

    try:
        # Create or update project webhook
        api_response = api_instance.configure_webhook(project_id, configure_webhook_request=configure_webhook_request)
        print("The response of WebhooksApi->configure_webhook:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling WebhooksApi->configure_webhook: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **str**|  | 
 **configure_webhook_request** | [**ConfigureWebhookRequest**](ConfigureWebhookRequest.md)|  | [optional] 

### Return type

[**ConfigureWebhook200Response**](ConfigureWebhook200Response.md)

### Authorization

[OrgBearerAuth](../README.md#OrgBearerAuth), [ApiKeyAuth](../README.md#ApiKeyAuth), [ProjectBearerAuth](../README.md#ProjectBearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Webhook configuration updated |  -  |
**403** | Project webhook limit reached for your plan |  -  |
**404** | Project not found |  -  |
**500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_webhook_config**
> GetWebhookConfig200Response get_webhook_config(project_id)

Get project webhook configuration

Get the current webhook URL, events, version, and transformations for a project.
This is **where Mudbase POSTs event payloads**; it does **not** return a `webhookId`. Delivery ids (`WebhookLog._id`) come from **`POST /api/webhooks/trigger`** or automatic deliveries, and from **list logs** endpoints.

Requires ProjectBearerAuth (JWT) or ApiKeyAuth (X-API-Key) with project read access.


### Example

* Bearer (JWT) Authentication (OrgBearerAuth):
* Api Key Authentication (ApiKeyAuth):
* Bearer (JWT) Authentication (ProjectBearerAuth):

```python
import mudbase
from mudbase.models.get_webhook_config200_response import GetWebhookConfig200Response
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
    api_instance = mudbase.WebhooksApi(api_client)
    project_id = 'project_id_example' # str | 

    try:
        # Get project webhook configuration
        api_response = api_instance.get_webhook_config(project_id)
        print("The response of WebhooksApi->get_webhook_config:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling WebhooksApi->get_webhook_config: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **str**|  | 

### Return type

[**GetWebhookConfig200Response**](GetWebhookConfig200Response.md)

### Authorization

[OrgBearerAuth](../README.md#OrgBearerAuth), [ApiKeyAuth](../README.md#ApiKeyAuth), [ProjectBearerAuth](../README.md#ProjectBearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Webhook configuration |  -  |
**404** | Project not found |  -  |
**500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_webhook_stats**
> WebhookStatsResponse get_webhook_stats(project_id=project_id, days=days)

Get webhook delivery statistics

Aggregates **`WebhookLog`** rows for your organization over the last **`days`** (default 7).
Optional **`projectId`** filters to a project in your org.

Returns **`statusStats`** (counts and average duration per delivery **status**) and **`eventStats`** (counts and success rate per **event** name).

**Auth:** Organization JWT only (`authRequired`).


### Example

* Bearer (JWT) Authentication (OrgBearerAuth):

```python
import mudbase
from mudbase.models.webhook_stats_response import WebhookStatsResponse
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
    api_instance = mudbase.WebhooksApi(api_client)
    project_id = 'project_id_example' # str | Optional; limit stats to this project. (optional)
    days = 7 # int |  (optional) (default to 7)

    try:
        # Get webhook delivery statistics
        api_response = api_instance.get_webhook_stats(project_id=project_id, days=days)
        print("The response of WebhooksApi->get_webhook_stats:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling WebhooksApi->get_webhook_stats: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **str**| Optional; limit stats to this project. | [optional] 
 **days** | **int**|  | [optional] [default to 7]

### Return type

[**WebhookStatsResponse**](WebhookStatsResponse.md)

### Authorization

[OrgBearerAuth](../README.md#OrgBearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Aggregated webhook log statistics |  -  |
**400** | Bad request |  -  |
**404** | Project not found or not in your org |  -  |
**500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_project_webhook_logs**
> WebhookListResponse list_project_webhook_logs(project_id, page=page, limit=limit, status=status, event=event)

List webhook delivery logs (project)

Same **`WebhookLog`** documents as **`GET /api/webhooks`**, scoped to **`projectId`** in the path.
Accepts **org JWT**, **project JWT**, or **project API key** with project read access.

Each item’s **`_id`** is the id returned as **`webhookId`** from **`POST /api/webhooks/trigger`** and used in **`POST /api/webhooks/retry/{webhookId}`**.


### Example

* Bearer (JWT) Authentication (OrgBearerAuth):
* Api Key Authentication (ApiKeyAuth):
* Bearer (JWT) Authentication (ProjectBearerAuth):

```python
import mudbase
from mudbase.models.webhook_list_response import WebhookListResponse
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
    api_instance = mudbase.WebhooksApi(api_client)
    project_id = 'project_id_example' # str | 
    page = 1 # int |  (optional) (default to 1)
    limit = 20 # int |  (optional) (default to 20)
    status = 'status_example' # str |  (optional)
    event = 'event_example' # str |  (optional)

    try:
        # List webhook delivery logs (project)
        api_response = api_instance.list_project_webhook_logs(project_id, page=page, limit=limit, status=status, event=event)
        print("The response of WebhooksApi->list_project_webhook_logs:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling WebhooksApi->list_project_webhook_logs: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **str**|  | 
 **page** | **int**|  | [optional] [default to 1]
 **limit** | **int**|  | [optional] [default to 20]
 **status** | **str**|  | [optional] 
 **event** | **str**|  | [optional] 

### Return type

[**WebhookListResponse**](WebhookListResponse.md)

### Authorization

[OrgBearerAuth](../README.md#OrgBearerAuth), [ApiKeyAuth](../README.md#ApiKeyAuth), [ProjectBearerAuth](../README.md#ProjectBearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Webhook delivery logs for the project |  -  |
**401** | Authentication required |  -  |
**403** | Access denied |  -  |
**500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_webhooks**
> WebhookListResponse list_webhooks(page=page, limit=limit, status=status, event=event, project_id=project_id)

List webhook delivery logs (organization)

Paginated **webhook delivery logs** for your organization (each row is one outbound HTTP attempt).
Optional **`projectId`** query filters to a project that belongs to your org.

Use each log document’s **`_id`** (MongoDB ObjectId) as **`webhookId`** when calling **`POST /api/webhooks/retry/{webhookId}`** after a failed delivery.
Organization **JWT only** (`OrgBearerAuth`); project API keys are not accepted on this route.


### Example

* Bearer (JWT) Authentication (OrgBearerAuth):

```python
import mudbase
from mudbase.models.webhook_list_response import WebhookListResponse
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
    api_instance = mudbase.WebhooksApi(api_client)
    page = 1 # int |  (optional) (default to 1)
    limit = 20 # int |  (optional) (default to 20)
    status = 'status_example' # str |  (optional)
    event = 'event_example' # str |  (optional)
    project_id = 'project_id_example' # str | Optional; restrict logs to this project (must belong to your org). (optional)

    try:
        # List webhook delivery logs (organization)
        api_response = api_instance.list_webhooks(page=page, limit=limit, status=status, event=event, project_id=project_id)
        print("The response of WebhooksApi->list_webhooks:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling WebhooksApi->list_webhooks: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **page** | **int**|  | [optional] [default to 1]
 **limit** | **int**|  | [optional] [default to 20]
 **status** | **str**|  | [optional] 
 **event** | **str**|  | [optional] 
 **project_id** | **str**| Optional; restrict logs to this project (must belong to your org). | [optional] 

### Return type

[**WebhookListResponse**](WebhookListResponse.md)

### Authorization

[OrgBearerAuth](../README.md#OrgBearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Webhook delivery logs |  -  |
**400** | Bad request |  -  |
**403** | Access denied |  -  |
**500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **retry_webhook**
> RetryWebhookResponse retry_webhook(webhook_id)

Retry a failed webhook delivery

**`webhookId`** (path) = **`WebhookLog._id`** (MongoDB ObjectId)—the same value returned as **`webhookId`** from **`POST /api/webhooks/trigger`** and as **`_id`** on **`GET /api/webhooks`** / **`GET /api/webhooks/projects/{projectId}`**.

**Not** the string **`webhookId`** field stored on the log document (e.g. `manual-173…`); use the document **`_id`** for this path.

Resets a non-success log to **pending** and re-delivers. **400** if status is already **`success`**.

**Auth:** Organization JWT only; project API keys are not accepted.


### Example

* Bearer (JWT) Authentication (OrgBearerAuth):

```python
import mudbase
from mudbase.models.retry_webhook_response import RetryWebhookResponse
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
    api_instance = mudbase.WebhooksApi(api_client)
    webhook_id = 'webhook_id_example' # str | WebhookLog document `_id` (delivery log id).

    try:
        # Retry a failed webhook delivery
        api_response = api_instance.retry_webhook(webhook_id)
        print("The response of WebhooksApi->retry_webhook:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling WebhooksApi->retry_webhook: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **webhook_id** | **str**| WebhookLog document &#x60;_id&#x60; (delivery log id). | 

### Return type

[**RetryWebhookResponse**](RetryWebhookResponse.md)

### Authorization

[OrgBearerAuth](../README.md#OrgBearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Retry queued |  -  |
**400** | Log already succeeded |  -  |
**401** | Authentication required |  -  |
**403** | Access denied |  -  |
**404** | Log not found or not in your org |  -  |
**500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **test_webhook_transformation**
> TestWebhookTransformation200Response test_webhook_transformation(project_id, test_webhook_transformation_request)

Test webhook transformation

Apply transformation rules to a sample payload and return original and transformed payloads.
Requires ProjectBearerAuth (JWT) or ApiKeyAuth (X-API-Key) with project update access.


### Example

* Bearer (JWT) Authentication (OrgBearerAuth):
* Api Key Authentication (ApiKeyAuth):
* Bearer (JWT) Authentication (ProjectBearerAuth):

```python
import mudbase
from mudbase.models.test_webhook_transformation200_response import TestWebhookTransformation200Response
from mudbase.models.test_webhook_transformation_request import TestWebhookTransformationRequest
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
    api_instance = mudbase.WebhooksApi(api_client)
    project_id = 'project_id_example' # str | 
    test_webhook_transformation_request = {"payload":{"event":"collection.insert","data":{"name":"Test"}},"transformations":[]} # TestWebhookTransformationRequest | 

    try:
        # Test webhook transformation
        api_response = api_instance.test_webhook_transformation(project_id, test_webhook_transformation_request)
        print("The response of WebhooksApi->test_webhook_transformation:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling WebhooksApi->test_webhook_transformation: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **str**|  | 
 **test_webhook_transformation_request** | [**TestWebhookTransformationRequest**](TestWebhookTransformationRequest.md)|  | 

### Return type

[**TestWebhookTransformation200Response**](TestWebhookTransformation200Response.md)

### Authorization

[OrgBearerAuth](../README.md#OrgBearerAuth), [ApiKeyAuth](../README.md#ApiKeyAuth), [ProjectBearerAuth](../README.md#ProjectBearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Transformation result |  -  |
**400** | payload and transformations are required |  -  |
**404** | Project not found |  -  |
**500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **trigger_webhook**
> TriggerWebhookResponse trigger_webhook(trigger_webhook_request)

Manually trigger an outbound webhook

Queues an HTTP delivery to **`url`** for **`projectId`** (must belong to your org). Creates a **`WebhookLog`** row, runs delivery, and returns the new log’s **`_id`**.

**Response field `webhookId`:** This is the **MongoDB `_id` of the delivery log** (same as the log’s **`_id`** in list endpoints). It is **not** part of the request body and is **not** the project `webhookSecret` from **`PUT .../config`**.

**Auth:** Org JWT, project JWT, or project API key with **project `update`** permission.


### Example

* Bearer (JWT) Authentication (OrgBearerAuth):
* Api Key Authentication (ApiKeyAuth):
* Bearer (JWT) Authentication (ProjectBearerAuth):

```python
import mudbase
from mudbase.models.trigger_webhook_request import TriggerWebhookRequest
from mudbase.models.trigger_webhook_response import TriggerWebhookResponse
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
    api_instance = mudbase.WebhooksApi(api_client)
    trigger_webhook_request = {"projectId":"65a1b2c3d4e5f6789012345b","url":"https://your-app.com/webhooks/mudbase","event":"manual.test","payload":{"message":"Hello from Mudbase"}} # TriggerWebhookRequest | 

    try:
        # Manually trigger an outbound webhook
        api_response = api_instance.trigger_webhook(trigger_webhook_request)
        print("The response of WebhooksApi->trigger_webhook:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling WebhooksApi->trigger_webhook: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **trigger_webhook_request** | [**TriggerWebhookRequest**](TriggerWebhookRequest.md)|  | 

### Return type

[**TriggerWebhookResponse**](TriggerWebhookResponse.md)

### Authorization

[OrgBearerAuth](../README.md#OrgBearerAuth), [ApiKeyAuth](../README.md#ApiKeyAuth), [ProjectBearerAuth](../README.md#ProjectBearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Delivery queued; **&#x60;webhookId&#x60;** is the new log document **&#x60;_id&#x60;** |  -  |
**400** | Missing projectId, invalid project id, or invalid URL (SSRF guard) |  -  |
**404** | Project not found or not in your org |  -  |
**500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

