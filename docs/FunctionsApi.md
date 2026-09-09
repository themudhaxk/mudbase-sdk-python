# mudbase.FunctionsApi

All URIs are relative to *https://cloud.mudbase.dev*

Method | HTTP request | Description
------------- | ------------- | -------------
[**activate_function**](FunctionsApi.md#activate_function) | **POST** /api/functions/projects/{projectId}/functions/{functionId}/activate | Activate function
[**create_function**](FunctionsApi.md#create_function) | **POST** /api/functions/projects/{projectId}/functions | Create function
[**deactivate_function**](FunctionsApi.md#deactivate_function) | **POST** /api/functions/projects/{projectId}/functions/{functionId}/deactivate | Deactivate function
[**delete_function**](FunctionsApi.md#delete_function) | **DELETE** /api/functions/projects/{projectId}/functions/{functionId} | Delete function
[**execute_function**](FunctionsApi.md#execute_function) | **POST** /api/functions/projects/{projectId}/functions/{functionId}/execute | Execute function
[**get_function**](FunctionsApi.md#get_function) | **GET** /api/functions/projects/{projectId}/functions/{functionId} | Get function
[**get_function_execution**](FunctionsApi.md#get_function_execution) | **GET** /api/functions/projects/{projectId}/functions/{functionId}/executions/{executionId} | Get execution status
[**get_function_logs**](FunctionsApi.md#get_function_logs) | **GET** /api/functions/projects/{projectId}/functions/{functionId}/logs | Get function execution logs
[**get_function_versions**](FunctionsApi.md#get_function_versions) | **GET** /api/functions/projects/{projectId}/functions/{functionId}/versions | Get function versions
[**list_functions**](FunctionsApi.md#list_functions) | **GET** /api/functions/projects/{projectId}/functions | List functions
[**retry_function_execution**](FunctionsApi.md#retry_function_execution) | **POST** /api/functions/projects/{projectId}/functions/{functionId}/retry/{executionIndex} | Retry failed execution
[**rollback_function**](FunctionsApi.md#rollback_function) | **POST** /api/functions/projects/{projectId}/functions/{functionId}/rollback | Rollback to previous version
[**simulate_function_trigger**](FunctionsApi.md#simulate_function_trigger) | **POST** /api/functions/projects/{projectId}/functions/{functionId}/simulate | Simulate trigger
[**trigger_function_webhook**](FunctionsApi.md#trigger_function_webhook) | **POST** /api/functions/webhook/{projectId} | Trigger webhook functions
[**update_function**](FunctionsApi.md#update_function) | **PUT** /api/functions/projects/{projectId}/functions/{functionId} | Update function


# **activate_function**
> FunctionResponse activate_function(project_id, function_id)

Activate function

Activate a deactivated function. Active functions can be triggered.

### Example

* Bearer (JWT) Authentication (OrgBearerAuth):
* Api Key Authentication (ApiKeyAuth):
* Bearer (JWT) Authentication (ProjectBearerAuth):

```python
import mudbase
from mudbase.models.function_response import FunctionResponse
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
    api_instance = mudbase.FunctionsApi(api_client)
    project_id = 'project_id_example' # str | 
    function_id = 'function_id_example' # str | 

    try:
        # Activate function
        api_response = api_instance.activate_function(project_id, function_id)
        print("The response of FunctionsApi->activate_function:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling FunctionsApi->activate_function: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **str**|  | 
 **function_id** | **str**|  | 

### Return type

[**FunctionResponse**](FunctionResponse.md)

### Authorization

[OrgBearerAuth](../README.md#OrgBearerAuth), [ApiKeyAuth](../README.md#ApiKeyAuth), [ProjectBearerAuth](../README.md#ProjectBearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Function activated |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **create_function**
> FunctionResponse create_function(project_id, create_function_request)

Create function

Create a new serverless function. Trigger types: http, document, file, webhook, cron, messaging.
Sandbox globals available today: `payload`, `context`, `env`, `console`. Function code runs in an
isolated worker with no ambient network or database access — it can only read its trigger payload,
the `env` vars you configure, and return a JSON-serializable result; it cannot yet call back into
your project's database, storage, or messaging APIs from inside the function body. If you
need to read or write project data from a function, call the regular REST API (with your own API
key) from your own backend in response to the function's returned result, rather than from within
the function's own code.


### Example

* Bearer (JWT) Authentication (OrgBearerAuth):
* Api Key Authentication (ApiKeyAuth):
* Bearer (JWT) Authentication (ProjectBearerAuth):

```python
import mudbase
from mudbase.models.create_function_request import CreateFunctionRequest
from mudbase.models.function_response import FunctionResponse
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
    api_instance = mudbase.FunctionsApi(api_client)
    project_id = 'project_id_example' # str | 
    create_function_request = {"name":"OnUserCreate","description":"Process new users","code":"// payload.document holds the created/updated document for this trigger\nconst created = payload.document?.data || {};\nconsole.log('New user document:', created.email);\nreturn { email: created.email || null, receivedAt: new Date().toISOString() };\n","trigger":{"type":"document","event":"create","collectionId":"685ada8fd9416ac02f171abf"},"environment":{"DEBUG":"true"}} # CreateFunctionRequest | 

    try:
        # Create function
        api_response = api_instance.create_function(project_id, create_function_request)
        print("The response of FunctionsApi->create_function:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling FunctionsApi->create_function: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **str**|  | 
 **create_function_request** | [**CreateFunctionRequest**](CreateFunctionRequest.md)|  | 

### Return type

[**FunctionResponse**](FunctionResponse.md)

### Authorization

[OrgBearerAuth](../README.md#OrgBearerAuth), [ApiKeyAuth](../README.md#ApiKeyAuth), [ProjectBearerAuth](../README.md#ProjectBearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | Function created |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **deactivate_function**
> FunctionResponse deactivate_function(project_id, function_id)

Deactivate function

Deactivate a function. Deactivated functions will not be triggered.

### Example

* Bearer (JWT) Authentication (OrgBearerAuth):
* Api Key Authentication (ApiKeyAuth):
* Bearer (JWT) Authentication (ProjectBearerAuth):

```python
import mudbase
from mudbase.models.function_response import FunctionResponse
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
    api_instance = mudbase.FunctionsApi(api_client)
    project_id = 'project_id_example' # str | 
    function_id = 'function_id_example' # str | 

    try:
        # Deactivate function
        api_response = api_instance.deactivate_function(project_id, function_id)
        print("The response of FunctionsApi->deactivate_function:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling FunctionsApi->deactivate_function: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **str**|  | 
 **function_id** | **str**|  | 

### Return type

[**FunctionResponse**](FunctionResponse.md)

### Authorization

[OrgBearerAuth](../README.md#OrgBearerAuth), [ApiKeyAuth](../README.md#ApiKeyAuth), [ProjectBearerAuth](../README.md#ProjectBearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Function deactivated |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_function**
> DeleteFunction200Response delete_function(project_id, function_id)

Delete function

Delete a function permanently. This is a destructive operation.

### Example

* Bearer (JWT) Authentication (OrgBearerAuth):
* Api Key Authentication (ApiKeyAuth):
* Bearer (JWT) Authentication (ProjectBearerAuth):

```python
import mudbase
from mudbase.models.delete_function200_response import DeleteFunction200Response
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
    api_instance = mudbase.FunctionsApi(api_client)
    project_id = 'project_id_example' # str | 
    function_id = 'function_id_example' # str | 

    try:
        # Delete function
        api_response = api_instance.delete_function(project_id, function_id)
        print("The response of FunctionsApi->delete_function:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling FunctionsApi->delete_function: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **str**|  | 
 **function_id** | **str**|  | 

### Return type

[**DeleteFunction200Response**](DeleteFunction200Response.md)

### Authorization

[OrgBearerAuth](../README.md#OrgBearerAuth), [ApiKeyAuth](../README.md#ApiKeyAuth), [ProjectBearerAuth](../README.md#ProjectBearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Function deleted |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **execute_function**
> FunctionExecutionResponse execute_function(project_id, function_id, execute_function_request=execute_function_request)

Execute function

Manually execute a function with custom payload. Payload is merged with auto-injected trigger context.
Rate limited (data mutation rate limiter). Enforces maxExecutionsPerMinute/maxExecutionsPerHour.

This endpoint is asynchronous: it returns 202 immediately with an `executionId`, before the
function has necessarily finished running. Poll
`GET /api/functions/projects/{projectId}/functions/{functionId}/executions/{executionId}`
until `status` leaves `queued`/`running` to get the real result, error, and duration.


### Example

* Bearer (JWT) Authentication (OrgBearerAuth):
* Api Key Authentication (ApiKeyAuth):
* Bearer (JWT) Authentication (ProjectBearerAuth):

```python
import mudbase
from mudbase.models.execute_function_request import ExecuteFunctionRequest
from mudbase.models.function_execution_response import FunctionExecutionResponse
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
    api_instance = mudbase.FunctionsApi(api_client)
    project_id = 'project_id_example' # str | 
    function_id = 'function_id_example' # str | 
    execute_function_request = {"payload":{"userId":"685acbe0e129932fbb7a0fc2","action":"process"}} # ExecuteFunctionRequest |  (optional)

    try:
        # Execute function
        api_response = api_instance.execute_function(project_id, function_id, execute_function_request=execute_function_request)
        print("The response of FunctionsApi->execute_function:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling FunctionsApi->execute_function: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **str**|  | 
 **function_id** | **str**|  | 
 **execute_function_request** | [**ExecuteFunctionRequest**](ExecuteFunctionRequest.md)|  | [optional] 

### Return type

[**FunctionExecutionResponse**](FunctionExecutionResponse.md)

### Authorization

[OrgBearerAuth](../README.md#OrgBearerAuth), [ApiKeyAuth](../README.md#ApiKeyAuth), [ProjectBearerAuth](../README.md#ProjectBearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**202** | Execution accepted (queued or run synchronously) — poll the executions endpoint for the outcome |  -  |
**400** | Payload exceeds the function&#39;s configured max payload size |  -  |
**429** | Rate limit exceeded (maxExecutionsPerMinute/maxExecutionsPerHour, or the data-mutation rate limiter) |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_function**
> FunctionResponse get_function(project_id, function_id)

Get function

Get function details by ID including createdBy/updatedBy.

### Example

* Bearer (JWT) Authentication (OrgBearerAuth):
* Api Key Authentication (ApiKeyAuth):
* Bearer (JWT) Authentication (ProjectBearerAuth):

```python
import mudbase
from mudbase.models.function_response import FunctionResponse
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
    api_instance = mudbase.FunctionsApi(api_client)
    project_id = 'project_id_example' # str | 
    function_id = 'function_id_example' # str | 

    try:
        # Get function
        api_response = api_instance.get_function(project_id, function_id)
        print("The response of FunctionsApi->get_function:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling FunctionsApi->get_function: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **str**|  | 
 **function_id** | **str**|  | 

### Return type

[**FunctionResponse**](FunctionResponse.md)

### Authorization

[OrgBearerAuth](../README.md#OrgBearerAuth), [ApiKeyAuth](../README.md#ApiKeyAuth), [ProjectBearerAuth](../README.md#ProjectBearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Function details |  -  |
**404** | Function not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_function_execution**
> FunctionExecutionStatusResponse get_function_execution(project_id, function_id, execution_id)

Get execution status

Poll this after Execute function or Simulate trigger to get the real outcome — both of
those endpoints return 202 immediately and do not carry the result themselves.
`status` is one of `queued`, `provisioning`, `running`, `success`, `failed`, `timeout`;
`result`/`error`/`durationMs`/`logs` are only populated once `status` leaves
`queued`/`running`.


### Example

* Bearer (JWT) Authentication (OrgBearerAuth):
* Api Key Authentication (ApiKeyAuth):
* Bearer (JWT) Authentication (ProjectBearerAuth):

```python
import mudbase
from mudbase.models.function_execution_status_response import FunctionExecutionStatusResponse
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
    api_instance = mudbase.FunctionsApi(api_client)
    project_id = 'project_id_example' # str | 
    function_id = 'function_id_example' # str | 
    execution_id = 'execution_id_example' # str | 

    try:
        # Get execution status
        api_response = api_instance.get_function_execution(project_id, function_id, execution_id)
        print("The response of FunctionsApi->get_function_execution:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling FunctionsApi->get_function_execution: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **str**|  | 
 **function_id** | **str**|  | 
 **execution_id** | **str**|  | 

### Return type

[**FunctionExecutionStatusResponse**](FunctionExecutionStatusResponse.md)

### Authorization

[OrgBearerAuth](../README.md#OrgBearerAuth), [ApiKeyAuth](../README.md#ApiKeyAuth), [ProjectBearerAuth](../README.md#ProjectBearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Execution status |  -  |
**404** | Execution not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_function_logs**
> FunctionLogsResponse get_function_logs(project_id, function_id, limit=limit, offset=offset)

Get function execution logs

Get execution logs with pagination. Includes stats (totalExecutions, successful, failed, successRate, avgExecutionTime, lastRun).

### Example

* Bearer (JWT) Authentication (OrgBearerAuth):
* Bearer (JWT) Authentication (ProjectBearerAuth):

```python
import mudbase
from mudbase.models.function_logs_response import FunctionLogsResponse
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

# Configure Bearer authorization (JWT): ProjectBearerAuth
configuration = mudbase.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with mudbase.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = mudbase.FunctionsApi(api_client)
    project_id = 'project_id_example' # str | 
    function_id = 'function_id_example' # str | 
    limit = 50 # int |  (optional) (default to 50)
    offset = 0 # int |  (optional) (default to 0)

    try:
        # Get function execution logs
        api_response = api_instance.get_function_logs(project_id, function_id, limit=limit, offset=offset)
        print("The response of FunctionsApi->get_function_logs:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling FunctionsApi->get_function_logs: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **str**|  | 
 **function_id** | **str**|  | 
 **limit** | **int**|  | [optional] [default to 50]
 **offset** | **int**|  | [optional] [default to 0]

### Return type

[**FunctionLogsResponse**](FunctionLogsResponse.md)

### Authorization

[OrgBearerAuth](../README.md#OrgBearerAuth), [ProjectBearerAuth](../README.md#ProjectBearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Function logs and stats |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_function_versions**
> GetFunctionVersions200Response get_function_versions(project_id, function_id)

Get function versions

List all code versions for a function. Used for rollback.

### Example

* Bearer (JWT) Authentication (OrgBearerAuth):
* Api Key Authentication (ApiKeyAuth):
* Bearer (JWT) Authentication (ProjectBearerAuth):

```python
import mudbase
from mudbase.models.get_function_versions200_response import GetFunctionVersions200Response
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
    api_instance = mudbase.FunctionsApi(api_client)
    project_id = 'project_id_example' # str | 
    function_id = 'function_id_example' # str | 

    try:
        # Get function versions
        api_response = api_instance.get_function_versions(project_id, function_id)
        print("The response of FunctionsApi->get_function_versions:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling FunctionsApi->get_function_versions: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **str**|  | 
 **function_id** | **str**|  | 

### Return type

[**GetFunctionVersions200Response**](GetFunctionVersions200Response.md)

### Authorization

[OrgBearerAuth](../README.md#OrgBearerAuth), [ApiKeyAuth](../README.md#ApiKeyAuth), [ProjectBearerAuth](../README.md#ProjectBearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Function versions |  -  |
**404** | Function not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_functions**
> FunctionListResponse list_functions(project_id, page=page, limit=limit, search=search, trigger_type=trigger_type, is_active=is_active)

List functions

List serverless functions in a project with optional search and filters.
Supports trigger types: http, event, document, file, webhook, cron, messaging.


### Example

* Bearer (JWT) Authentication (OrgBearerAuth):
* Api Key Authentication (ApiKeyAuth):
* Bearer (JWT) Authentication (ProjectBearerAuth):

```python
import mudbase
from mudbase.models.function_list_response import FunctionListResponse
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
    api_instance = mudbase.FunctionsApi(api_client)
    project_id = 'project_id_example' # str | 
    page = 1 # int |  (optional) (default to 1)
    limit = 20 # int |  (optional) (default to 20)
    search = 'search_example' # str | Search by name or description (optional)
    trigger_type = 'trigger_type_example' # str | Filter by trigger type (optional)
    is_active = True # bool | Filter by active status (true/false) (optional)

    try:
        # List functions
        api_response = api_instance.list_functions(project_id, page=page, limit=limit, search=search, trigger_type=trigger_type, is_active=is_active)
        print("The response of FunctionsApi->list_functions:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling FunctionsApi->list_functions: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **str**|  | 
 **page** | **int**|  | [optional] [default to 1]
 **limit** | **int**|  | [optional] [default to 20]
 **search** | **str**| Search by name or description | [optional] 
 **trigger_type** | **str**| Filter by trigger type | [optional] 
 **is_active** | **bool**| Filter by active status (true/false) | [optional] 

### Return type

[**FunctionListResponse**](FunctionListResponse.md)

### Authorization

[OrgBearerAuth](../README.md#OrgBearerAuth), [ApiKeyAuth](../README.md#ApiKeyAuth), [ProjectBearerAuth](../README.md#ProjectBearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Functions list |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **retry_function_execution**
> FunctionExecutionResponse retry_function_execution(project_id, function_id, execution_index)

Retry failed execution

Retry a failed execution by its index (0-based) in the logs. Cannot retry successful executions.

### Example

* Bearer (JWT) Authentication (OrgBearerAuth):
* Api Key Authentication (ApiKeyAuth):
* Bearer (JWT) Authentication (ProjectBearerAuth):

```python
import mudbase
from mudbase.models.function_execution_response import FunctionExecutionResponse
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
    api_instance = mudbase.FunctionsApi(api_client)
    project_id = 'project_id_example' # str | 
    function_id = 'function_id_example' # str | 
    execution_index = 56 # int | 0-based index of the execution in logs

    try:
        # Retry failed execution
        api_response = api_instance.retry_function_execution(project_id, function_id, execution_index)
        print("The response of FunctionsApi->retry_function_execution:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling FunctionsApi->retry_function_execution: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **str**|  | 
 **function_id** | **str**|  | 
 **execution_index** | **int**| 0-based index of the execution in logs | 

### Return type

[**FunctionExecutionResponse**](FunctionExecutionResponse.md)

### Authorization

[OrgBearerAuth](../README.md#OrgBearerAuth), [ApiKeyAuth](../README.md#ApiKeyAuth), [ProjectBearerAuth](../README.md#ProjectBearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Retry result |  -  |
**400** | Cannot retry successful execution |  -  |
**404** | Function or execution not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **rollback_function**
> FunctionResponse rollback_function(project_id, function_id, rollback_function_request)

Rollback to previous version

Rollback function code to a previous version. Version number is required.

### Example

* Bearer (JWT) Authentication (OrgBearerAuth):
* Api Key Authentication (ApiKeyAuth):
* Bearer (JWT) Authentication (ProjectBearerAuth):

```python
import mudbase
from mudbase.models.function_response import FunctionResponse
from mudbase.models.rollback_function_request import RollbackFunctionRequest
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
    api_instance = mudbase.FunctionsApi(api_client)
    project_id = 'project_id_example' # str | 
    function_id = 'function_id_example' # str | 
    rollback_function_request = {"version":2} # RollbackFunctionRequest | 

    try:
        # Rollback to previous version
        api_response = api_instance.rollback_function(project_id, function_id, rollback_function_request)
        print("The response of FunctionsApi->rollback_function:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling FunctionsApi->rollback_function: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **str**|  | 
 **function_id** | **str**|  | 
 **rollback_function_request** | [**RollbackFunctionRequest**](RollbackFunctionRequest.md)|  | 

### Return type

[**FunctionResponse**](FunctionResponse.md)

### Authorization

[OrgBearerAuth](../README.md#OrgBearerAuth), [ApiKeyAuth](../README.md#ApiKeyAuth), [ProjectBearerAuth](../README.md#ProjectBearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Function rolled back |  -  |
**400** | Version number is required |  -  |
**404** | Function or version not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **simulate_function_trigger**
> FunctionExecutionResponse simulate_function_trigger(project_id, function_id, simulate_function_trigger_request=simulate_function_trigger_request)

Simulate trigger

Test a function with simulated trigger context. Use to verify document, file, webhook, or cron payloads.
Executes the function with the provided eventContext merged into the payload.

Asynchronous, same pattern as Execute function: returns 202 immediately with an `executionId`.
Poll `GET /api/functions/projects/{projectId}/functions/{functionId}/executions/{executionId}`
for the real result.


### Example

* Bearer (JWT) Authentication (OrgBearerAuth):
* Api Key Authentication (ApiKeyAuth):
* Bearer (JWT) Authentication (ProjectBearerAuth):

```python
import mudbase
from mudbase.models.function_execution_response import FunctionExecutionResponse
from mudbase.models.simulate_function_trigger_request import SimulateFunctionTriggerRequest
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
    api_instance = mudbase.FunctionsApi(api_client)
    project_id = 'project_id_example' # str | 
    function_id = 'function_id_example' # str | 
    simulate_function_trigger_request = {"trigger":{"type":"document","event":"create"},"eventContext":{"document":{"_id":"685ae1210136e73fa1dcaf36","collectionId":"685ada8fd9416ac02f171abf","data":{"name":"John","email":"john@example.com"}}}} # SimulateFunctionTriggerRequest |  (optional)

    try:
        # Simulate trigger
        api_response = api_instance.simulate_function_trigger(project_id, function_id, simulate_function_trigger_request=simulate_function_trigger_request)
        print("The response of FunctionsApi->simulate_function_trigger:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling FunctionsApi->simulate_function_trigger: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **str**|  | 
 **function_id** | **str**|  | 
 **simulate_function_trigger_request** | [**SimulateFunctionTriggerRequest**](SimulateFunctionTriggerRequest.md)|  | [optional] 

### Return type

[**FunctionExecutionResponse**](FunctionExecutionResponse.md)

### Authorization

[OrgBearerAuth](../README.md#OrgBearerAuth), [ApiKeyAuth](../README.md#ApiKeyAuth), [ProjectBearerAuth](../README.md#ProjectBearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**202** | Simulation accepted — poll the executions endpoint for the outcome |  -  |
**404** | Function not found or inactive |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **trigger_function_webhook**
> TriggerFunctionWebhook200Response trigger_function_webhook(project_id, x_webhook_secret=x_webhook_secret, body=body)

Trigger webhook functions

Public endpoint for external services to trigger functions with `trigger.type: webhook`.
No authentication required. Optionally verify using `X-Webhook-Secret` header (configure per project or via FUNCTION_WEBHOOK_SECRET).
Rate limited to 120 requests per 15 minutes per IP (per-org adjustable).


### Example


```python
import mudbase
from mudbase.models.trigger_function_webhook200_response import TriggerFunctionWebhook200Response
from mudbase.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://cloud.mudbase.dev
# See configuration.py for a list of all supported configuration parameters.
configuration = mudbase.Configuration(
    host = "https://cloud.mudbase.dev"
)


# Enter a context with an instance of the API client
with mudbase.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = mudbase.FunctionsApi(api_client)
    project_id = 'project_id_example' # str | 
    x_webhook_secret = 'x_webhook_secret_example' # str | Optional webhook secret for verification (optional)
    body = {"event":"user.created","userId":"507f1f77bcf86cd799439011","timestamp":"2026-04-03T12:00:00.000Z"} # object |  (optional)

    try:
        # Trigger webhook functions
        api_response = api_instance.trigger_function_webhook(project_id, x_webhook_secret=x_webhook_secret, body=body)
        print("The response of FunctionsApi->trigger_function_webhook:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling FunctionsApi->trigger_function_webhook: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **str**|  | 
 **x_webhook_secret** | **str**| Optional webhook secret for verification | [optional] 
 **body** | **object**|  | [optional] 

### Return type

[**TriggerFunctionWebhook200Response**](TriggerFunctionWebhook200Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json, application/x-www-form-urlencoded, text/plain
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Functions triggered successfully |  -  |
**400** | Invalid project ID |  -  |
**401** | Invalid webhook secret |  -  |
**404** | Project not found |  -  |
**429** | Rate limit exceeded |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_function**
> FunctionResponse update_function(project_id, function_id, update_function_request=update_function_request)

Update function

Update function configuration. Code changes are versioned automatically.

### Example

* Bearer (JWT) Authentication (OrgBearerAuth):
* Api Key Authentication (ApiKeyAuth):
* Bearer (JWT) Authentication (ProjectBearerAuth):

```python
import mudbase
from mudbase.models.function_response import FunctionResponse
from mudbase.models.update_function_request import UpdateFunctionRequest
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
    api_instance = mudbase.FunctionsApi(api_client)
    project_id = 'project_id_example' # str | 
    function_id = 'function_id_example' # str | 
    update_function_request = {"name":"OnUserCreate v2","code":"return { version: 2 };\n","versionComment":"Add version tracking"} # UpdateFunctionRequest |  (optional)

    try:
        # Update function
        api_response = api_instance.update_function(project_id, function_id, update_function_request=update_function_request)
        print("The response of FunctionsApi->update_function:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling FunctionsApi->update_function: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **str**|  | 
 **function_id** | **str**|  | 
 **update_function_request** | [**UpdateFunctionRequest**](UpdateFunctionRequest.md)|  | [optional] 

### Return type

[**FunctionResponse**](FunctionResponse.md)

### Authorization

[OrgBearerAuth](../README.md#OrgBearerAuth), [ApiKeyAuth](../README.md#ApiKeyAuth), [ProjectBearerAuth](../README.md#ProjectBearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Function updated |  -  |
**404** | Function not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

