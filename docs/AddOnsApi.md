# mudbase.AddOnsApi

All URIs are relative to *https://cloud.mudbase.dev*

Method | HTTP request | Description
------------- | ------------- | -------------
[**api_addons_get**](AddOnsApi.md#api_addons_get) | **GET** /api/addons | List the add-on catalog
[**api_projects_project_id_addons_addon_invoke_post**](AddOnsApi.md#api_projects_project_id_addons_addon_invoke_post) | **POST** /api/projects/{projectId}/addons/{addon}/invoke | Invoke an add-on for a project
[**api_projects_project_id_addons_jobs_id_get**](AddOnsApi.md#api_projects_project_id_addons_jobs_id_get) | **GET** /api/projects/{projectId}/addons/jobs/{id} | Get an add-on job status


# **api_addons_get**
> ApiAddonsGet200Response api_addons_get()

List the add-on catalog

Returns the available add-ons (key, metadata, pricing) the caller can invoke.

### Example

* Bearer (JWT) Authentication (OrgBearerAuth):

```python
import mudbase
from mudbase.models.api_addons_get200_response import ApiAddonsGet200Response
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
    api_instance = mudbase.AddOnsApi(api_client)

    try:
        # List the add-on catalog
        api_response = api_instance.api_addons_get()
        print("The response of AddOnsApi->api_addons_get:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AddOnsApi->api_addons_get: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

[**ApiAddonsGet200Response**](ApiAddonsGet200Response.md)

### Authorization

[OrgBearerAuth](../README.md#OrgBearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Add-on catalog |  -  |
**401** | Authentication required |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **api_projects_project_id_addons_addon_invoke_post**
> ApiProjectsProjectIdAddonsAddonInvokePost200Response api_projects_project_id_addons_addon_invoke_post(project_id, addon, body=body)

Invoke an add-on for a project

Runs the named add-on against the project. Returns the job synchronously (200) when it completes immediately, or 202 with a pending job when processing continues in the background.

### Example

* Api Key Authentication (ApiKeyAuth):
* Bearer (JWT) Authentication (ProjectBearerAuth):

```python
import mudbase
from mudbase.models.api_projects_project_id_addons_addon_invoke_post200_response import ApiProjectsProjectIdAddonsAddonInvokePost200Response
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
    api_instance = mudbase.AddOnsApi(api_client)
    project_id = 'project_id_example' # str | 
    addon = 'addon_example' # str | Add-on key from the catalog.
    body = None # object |  (optional)

    try:
        # Invoke an add-on for a project
        api_response = api_instance.api_projects_project_id_addons_addon_invoke_post(project_id, addon, body=body)
        print("The response of AddOnsApi->api_projects_project_id_addons_addon_invoke_post:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AddOnsApi->api_projects_project_id_addons_addon_invoke_post: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **str**|  | 
 **addon** | **str**| Add-on key from the catalog. | 
 **body** | **object**|  | [optional] 

### Return type

[**ApiProjectsProjectIdAddonsAddonInvokePost200Response**](ApiProjectsProjectIdAddonsAddonInvokePost200Response.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [ProjectBearerAuth](../README.md#ProjectBearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Add-on job completed |  -  |
**202** | Add-on job accepted and processing |  -  |
**400** | Invalid add-on key or input |  -  |
**401** | Authentication required |  -  |
**403** | Project ownership required |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **api_projects_project_id_addons_jobs_id_get**
> ApiProjectsProjectIdAddonsAddonInvokePost200Response api_projects_project_id_addons_jobs_id_get(project_id, id)

Get an add-on job status

### Example

* Api Key Authentication (ApiKeyAuth):
* Bearer (JWT) Authentication (ProjectBearerAuth):

```python
import mudbase
from mudbase.models.api_projects_project_id_addons_addon_invoke_post200_response import ApiProjectsProjectIdAddonsAddonInvokePost200Response
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
    api_instance = mudbase.AddOnsApi(api_client)
    project_id = 'project_id_example' # str | 
    id = 'id_example' # str | Add-on job id.

    try:
        # Get an add-on job status
        api_response = api_instance.api_projects_project_id_addons_jobs_id_get(project_id, id)
        print("The response of AddOnsApi->api_projects_project_id_addons_jobs_id_get:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AddOnsApi->api_projects_project_id_addons_jobs_id_get: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **str**|  | 
 **id** | **str**| Add-on job id. | 

### Return type

[**ApiProjectsProjectIdAddonsAddonInvokePost200Response**](ApiProjectsProjectIdAddonsAddonInvokePost200Response.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [ProjectBearerAuth](../README.md#ProjectBearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The add-on job |  -  |
**401** | Authentication required |  -  |
**403** | Project ownership required |  -  |
**404** | Add-on job not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

