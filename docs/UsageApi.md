# mudbase.UsageApi

All URIs are relative to *https://cloud.mudbase.dev*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_overage**](UsageApi.md#get_overage) | **GET** /api/usage/overage | Get current overage line items
[**get_project_usage_stats**](UsageApi.md#get_project_usage_stats) | **GET** /api/usage/projects/{projectId} | Get project usage
[**get_project_usage_summary**](UsageApi.md#get_project_usage_summary) | **GET** /api/usage/projects/{projectId}/summary | Project dashboard usage summary
[**get_usage**](UsageApi.md#get_usage) | **GET** /api/usage | Get organization usage
[**get_usage_trends**](UsageApi.md#get_usage_trends) | **GET** /api/usage/trends | Get usage trends
[**get_usage_warnings**](UsageApi.md#get_usage_warnings) | **GET** /api/usage/warnings | Get usage warnings


# **get_overage**
> GetOverage200Response get_overage()

Get current overage line items

Returns overage line items for the authenticated organization's current billing period (current month).
Used by dashboards and billing UIs. Requires org-level JWT (authRequired).


### Example

* Bearer (JWT) Authentication (OrgBearerAuth):

```python
import mudbase
from mudbase.models.get_overage200_response import GetOverage200Response
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
    api_instance = mudbase.UsageApi(api_client)

    try:
        # Get current overage line items
        api_response = api_instance.get_overage()
        print("The response of UsageApi->get_overage:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling UsageApi->get_overage: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

[**GetOverage200Response**](GetOverage200Response.md)

### Authorization

[OrgBearerAuth](../README.md#OrgBearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Overage line items for current period |  -  |
**400** | Bad request |  -  |
**401** | Authentication required |  -  |
**503** | Service temporarily unavailable. Returned when the organization is restricted (e.g. suspended due to unpaid overage, spend limit exceeded, or API usage limit reached). End-users see a generic message; the real reason is logged server-side only.  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_project_usage_stats**
> ProjectUsageStatsResponse get_project_usage_stats(project_id, period=period)

Get project usage

Get usage statistics for a project (API calls, storage, bandwidth, database operations).
Accepts: OrgBearerAuth (for admin users), ProjectBearerAuth (JWT for authenticated users), or ApiKeyAuth (X-API-Key for programmatic access). Both ProjectBearerAuth and ApiKeyAuth are fully implemented.


### Example

* Bearer (JWT) Authentication (OrgBearerAuth):
* Bearer (JWT) Authentication (ProjectBearerAuth):

```python
import mudbase
from mudbase.models.project_usage_stats_response import ProjectUsageStatsResponse
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
    api_instance = mudbase.UsageApi(api_client)
    project_id = 'project_id_example' # str | 
    period = month # str |  (optional) (default to month)

    try:
        # Get project usage
        api_response = api_instance.get_project_usage_stats(project_id, period=period)
        print("The response of UsageApi->get_project_usage_stats:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling UsageApi->get_project_usage_stats: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **str**|  | 
 **period** | **str**|  | [optional] [default to month]

### Return type

[**ProjectUsageStatsResponse**](ProjectUsageStatsResponse.md)

### Authorization

[OrgBearerAuth](../README.md#OrgBearerAuth), [ProjectBearerAuth](../README.md#ProjectBearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Project usage statistics |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_project_usage_summary**
> ProjectUsageSummaryResponse get_project_usage_summary(project_id)

Project dashboard usage summary

Lightweight dashboard metrics for a project: requests today vs yesterday with % change, active users (24h/7d/30d),
7d active-user trend, 14-day request volume series, per-project openapi-docs latency (today/7d), and uptime (30d) from org HTTP non-5xx when enough samples else DB heartbeats.
Same auth as GET /api/usage/projects/{projectId} (org JWT, project JWT, or API key scoped to the project).


### Example

* Bearer (JWT) Authentication (OrgBearerAuth):
* Api Key Authentication (ApiKeyAuth):
* Bearer (JWT) Authentication (ProjectBearerAuth):

```python
import mudbase
from mudbase.models.project_usage_summary_response import ProjectUsageSummaryResponse
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
    api_instance = mudbase.UsageApi(api_client)
    project_id = 'project_id_example' # str | 

    try:
        # Project dashboard usage summary
        api_response = api_instance.get_project_usage_summary(project_id)
        print("The response of UsageApi->get_project_usage_summary:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling UsageApi->get_project_usage_summary: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **str**|  | 

### Return type

[**ProjectUsageSummaryResponse**](ProjectUsageSummaryResponse.md)

### Authorization

[OrgBearerAuth](../README.md#OrgBearerAuth), [ApiKeyAuth](../README.md#ApiKeyAuth), [ProjectBearerAuth](../README.md#ProjectBearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Summary payload |  -  |
**401** | Authentication required |  -  |
**404** | Resource not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_usage**
> UsageStatsResponse get_usage(period=period, start_date=start_date, end_date=end_date)

Get organization usage

### Example

* Bearer (JWT) Authentication (OrgBearerAuth):
* Bearer (JWT) Authentication (ProjectBearerAuth):

```python
import mudbase
from mudbase.models.usage_stats_response import UsageStatsResponse
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
    api_instance = mudbase.UsageApi(api_client)
    period = month # str |  (optional) (default to month)
    start_date = '2013-10-20T19:20:30+01:00' # datetime |  (optional)
    end_date = '2013-10-20T19:20:30+01:00' # datetime |  (optional)

    try:
        # Get organization usage
        api_response = api_instance.get_usage(period=period, start_date=start_date, end_date=end_date)
        print("The response of UsageApi->get_usage:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling UsageApi->get_usage: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **period** | **str**|  | [optional] [default to month]
 **start_date** | **datetime**|  | [optional] 
 **end_date** | **datetime**|  | [optional] 

### Return type

[**UsageStatsResponse**](UsageStatsResponse.md)

### Authorization

[OrgBearerAuth](../README.md#OrgBearerAuth), [ProjectBearerAuth](../README.md#ProjectBearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Usage statistics |  -  |
**503** | Service temporarily unavailable. Returned when the organization is restricted (e.g. suspended due to unpaid overage, spend limit exceeded, or API usage limit reached). End-users see a generic message; the real reason is logged server-side only.  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_usage_trends**
> UsageTrendsResponse get_usage_trends(days=days)

Get usage trends

Get usage trends over time for the authenticated organization or project.
Accepts: OrgBearerAuth (for admin users), ProjectBearerAuth (JWT for authenticated users), or ApiKeyAuth (X-API-Key for programmatic access). Both ProjectBearerAuth and ApiKeyAuth are fully implemented.


### Example

* Bearer (JWT) Authentication (OrgBearerAuth):
* Bearer (JWT) Authentication (ProjectBearerAuth):

```python
import mudbase
from mudbase.models.usage_trends_response import UsageTrendsResponse
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
    api_instance = mudbase.UsageApi(api_client)
    days = 30 # int |  (optional) (default to 30)

    try:
        # Get usage trends
        api_response = api_instance.get_usage_trends(days=days)
        print("The response of UsageApi->get_usage_trends:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling UsageApi->get_usage_trends: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **days** | **int**|  | [optional] [default to 30]

### Return type

[**UsageTrendsResponse**](UsageTrendsResponse.md)

### Authorization

[OrgBearerAuth](../README.md#OrgBearerAuth), [ProjectBearerAuth](../README.md#ProjectBearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Usage trends |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_usage_warnings**
> GetUsageWarnings200Response get_usage_warnings()

Get usage warnings

Returns usage warnings for the authenticated org (e.g. at 80% and 95% of plan limits). Requires org-level JWT.

### Example

* Bearer (JWT) Authentication (OrgBearerAuth):

```python
import mudbase
from mudbase.models.get_usage_warnings200_response import GetUsageWarnings200Response
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
    api_instance = mudbase.UsageApi(api_client)

    try:
        # Get usage warnings
        api_response = api_instance.get_usage_warnings()
        print("The response of UsageApi->get_usage_warnings:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling UsageApi->get_usage_warnings: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

[**GetUsageWarnings200Response**](GetUsageWarnings200Response.md)

### Authorization

[OrgBearerAuth](../README.md#OrgBearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Usage warnings |  -  |
**400** | Organization required |  -  |
**401** | Authentication required |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

