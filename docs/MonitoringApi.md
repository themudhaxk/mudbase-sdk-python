# mudbase.MonitoringApi

All URIs are relative to *https://cloud.mudbase.dev*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_monitoring_alert**](MonitoringApi.md#create_monitoring_alert) | **POST** /api/monitoring/alerts | Create monitoring alert
[**get_monitoring_analytics**](MonitoringApi.md#get_monitoring_analytics) | **GET** /api/monitoring/analytics | Get usage analytics (time series)
[**get_monitoring_errors**](MonitoringApi.md#get_monitoring_errors) | **GET** /api/monitoring/errors | Get error logs
[**get_monitoring_latency_insights**](MonitoringApi.md#get_monitoring_latency_insights) | **GET** /api/monitoring/latency-insights | Latency insights (route templates, percentiles, impact scores)
[**get_monitoring_logs**](MonitoringApi.md#get_monitoring_logs) | **GET** /api/monitoring/logs | Get audit logs
[**get_monitoring_performance**](MonitoringApi.md#get_monitoring_performance) | **GET** /api/monitoring/performance | Get performance metrics
[**get_monitoring_queue_metrics**](MonitoringApi.md#get_monitoring_queue_metrics) | **GET** /api/monitoring/queue-metrics | Usage metering queue job counts
[**list_monitoring_alerts**](MonitoringApi.md#list_monitoring_alerts) | **GET** /api/monitoring/alerts | List monitoring alerts


# **create_monitoring_alert**
> create_monitoring_alert(create_monitoring_alert_request)

Create monitoring alert

Create a monitoring alert (plan limit alertsPerProject enforced).

### Example

* Bearer (JWT) Authentication (OrgBearerAuth):

```python
import mudbase
from mudbase.models.create_monitoring_alert_request import CreateMonitoringAlertRequest
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
    api_instance = mudbase.MonitoringApi(api_client)
    create_monitoring_alert_request = {"name":"name_example","condition":"condition_example","threshold":0.01,"action":"action_example","projectId":"projectId_example"} # CreateMonitoringAlertRequest | 

    try:
        # Create monitoring alert
        api_instance.create_monitoring_alert(create_monitoring_alert_request)
    except Exception as e:
        print("Exception when calling MonitoringApi->create_monitoring_alert: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **create_monitoring_alert_request** | [**CreateMonitoringAlertRequest**](CreateMonitoringAlertRequest.md)|  | 

### Return type

void (empty response body)

### Authorization

[OrgBearerAuth](../README.md#OrgBearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | Alert created |  -  |
**401** | Authentication required |  -  |
**403** | Alert limit reached for your plan |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_monitoring_analytics**
> MonitoringAnalyticsResponse get_monitoring_analytics(project_id=project_id, period=period, granularity=granularity, days=days)

Get usage analytics (time series)

Aggregates UsageStat by day/week/month. Optional **projectId** scopes to one project.
Query **days** (1–90) for a rolling window (e.g. **days=14**); when set, overrides **period**.


### Example

* Bearer (JWT) Authentication (OrgBearerAuth):

```python
import mudbase
from mudbase.models.monitoring_analytics_response import MonitoringAnalyticsResponse
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
    api_instance = mudbase.MonitoringApi(api_client)
    project_id = 'project_id_example' # str |  (optional)
    period = month # str |  (optional) (default to month)
    granularity = day # str |  (optional) (default to day)
    days = 56 # int | Rolling window in days (1–90); when set, period becomes last_N_days (optional)

    try:
        # Get usage analytics (time series)
        api_response = api_instance.get_monitoring_analytics(project_id=project_id, period=period, granularity=granularity, days=days)
        print("The response of MonitoringApi->get_monitoring_analytics:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling MonitoringApi->get_monitoring_analytics: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **str**|  | [optional] 
 **period** | **str**|  | [optional] [default to month]
 **granularity** | **str**|  | [optional] [default to day]
 **days** | **int**| Rolling window in days (1–90); when set, period becomes last_N_days | [optional] 

### Return type

[**MonitoringAnalyticsResponse**](MonitoringAnalyticsResponse.md)

### Authorization

[OrgBearerAuth](../README.md#OrgBearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Stats series and totals |  -  |
**401** | Authentication required |  -  |
**404** | Project not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_monitoring_errors**
> get_monitoring_errors()

Get error logs

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
    api_instance = mudbase.MonitoringApi(api_client)

    try:
        # Get error logs
        api_instance.get_monitoring_errors()
    except Exception as e:
        print("Exception when calling MonitoringApi->get_monitoring_errors: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

void (empty response body)

### Authorization

[OrgBearerAuth](../README.md#OrgBearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Error logs |  -  |
**401** | Authentication required |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_monitoring_latency_insights**
> get_monitoring_latency_insights()

Latency insights (route templates, percentiles, impact scores)

Per-process snapshot: normalized **routeKey** (METHOD + path template), **p50/p95/p99**, 4xx/5xx counts,
**impactScore**, **alertsSuggested**, **rps**, **inFlight**, **eventLoopLagP99Ms**. One buffer per server instance.


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
    api_instance = mudbase.MonitoringApi(api_client)

    try:
        # Latency insights (route templates, percentiles, impact scores)
        api_instance.get_monitoring_latency_insights()
    except Exception as e:
        print("Exception when calling MonitoringApi->get_monitoring_latency_insights: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

void (empty response body)

### Authorization

[OrgBearerAuth](../README.md#OrgBearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Latency insights payload |  -  |
**401** | Authentication required |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_monitoring_logs**
> MonitoringLogsResponse get_monitoring_logs(page=page, limit=limit, project_id=project_id, user_id=user_id, level=level, start_date=start_date, end_date=end_date, action=action, resource=resource)

Get audit logs

Paginated audit trail for the org. Use **projectId** to scope to one project; **level=all** or **audit** for full activity feed.
Each entry includes **activityTitle** and **activityDetail** for dashboard copy. Requires monitoring read permission.


### Example

* Bearer (JWT) Authentication (OrgBearerAuth):

```python
import mudbase
from mudbase.models.monitoring_logs_response import MonitoringLogsResponse
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
    api_instance = mudbase.MonitoringApi(api_client)
    page = 1 # int |  (optional) (default to 1)
    limit = 20 # int |  (optional) (default to 20)
    project_id = 'project_id_example' # str | Filter to this project (must belong to org) (optional)
    user_id = 'user_id_example' # str | Filter to this user's audit entries (optional)
    level = 'error' # str | error|security|all|audit|low|medium|high|critical (optional) (default to 'error')
    start_date = '2013-10-20T19:20:30+01:00' # datetime |  (optional)
    end_date = '2013-10-20T19:20:30+01:00' # datetime |  (optional)
    action = 'action_example' # str |  (optional)
    resource = 'resource_example' # str |  (optional)

    try:
        # Get audit logs
        api_response = api_instance.get_monitoring_logs(page=page, limit=limit, project_id=project_id, user_id=user_id, level=level, start_date=start_date, end_date=end_date, action=action, resource=resource)
        print("The response of MonitoringApi->get_monitoring_logs:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling MonitoringApi->get_monitoring_logs: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **page** | **int**|  | [optional] [default to 1]
 **limit** | **int**|  | [optional] [default to 20]
 **project_id** | **str**| Filter to this project (must belong to org) | [optional] 
 **user_id** | **str**| Filter to this user&#39;s audit entries | [optional] 
 **level** | **str**| error|security|all|audit|low|medium|high|critical | [optional] [default to &#39;error&#39;]
 **start_date** | **datetime**|  | [optional] 
 **end_date** | **datetime**|  | [optional] 
 **action** | **str**|  | [optional] 
 **resource** | **str**|  | [optional] 

### Return type

[**MonitoringLogsResponse**](MonitoringLogsResponse.md)

### Authorization

[OrgBearerAuth](../README.md#OrgBearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Audit logs with pagination |  -  |
**400** | Invalid userId format |  -  |
**401** | Authentication required |  -  |
**404** | Project not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_monitoring_performance**
> MonitoringPerformanceResponse get_monitoring_performance(project_id=project_id, period=period)

Get performance metrics

Response time stats from AuditLog where available. With **projectId**, falls back to UsageStat latency averages
when audit data is sparse (**latencySource** may be **usage_stat**).


### Example

* Bearer (JWT) Authentication (OrgBearerAuth):

```python
import mudbase
from mudbase.models.monitoring_performance_response import MonitoringPerformanceResponse
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
    api_instance = mudbase.MonitoringApi(api_client)
    project_id = 'project_id_example' # str |  (optional)
    period = hour # str |  (optional) (default to hour)

    try:
        # Get performance metrics
        api_response = api_instance.get_monitoring_performance(project_id=project_id, period=period)
        print("The response of MonitoringApi->get_monitoring_performance:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling MonitoringApi->get_monitoring_performance: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **str**|  | [optional] 
 **period** | **str**|  | [optional] [default to hour]

### Return type

[**MonitoringPerformanceResponse**](MonitoringPerformanceResponse.md)

### Authorization

[OrgBearerAuth](../README.md#OrgBearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Performance metrics |  -  |
**401** | Authentication required |  -  |
**404** | Project not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_monitoring_queue_metrics**
> get_monitoring_queue_metrics()

Usage metering queue job counts

BullMQ **usage-events** queue counts when `USE_METERING_QUEUE` and `REDIS_URL` are set.

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
    api_instance = mudbase.MonitoringApi(api_client)

    try:
        # Usage metering queue job counts
        api_instance.get_monitoring_queue_metrics()
    except Exception as e:
        print("Exception when calling MonitoringApi->get_monitoring_queue_metrics: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

void (empty response body)

### Authorization

[OrgBearerAuth](../README.md#OrgBearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Queue depth snapshot |  -  |
**401** | Authentication required |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_monitoring_alerts**
> list_monitoring_alerts()

List monitoring alerts

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
    api_instance = mudbase.MonitoringApi(api_client)

    try:
        # List monitoring alerts
        api_instance.list_monitoring_alerts()
    except Exception as e:
        print("Exception when calling MonitoringApi->list_monitoring_alerts: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

void (empty response body)

### Authorization

[OrgBearerAuth](../README.md#OrgBearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | List of alerts |  -  |
**401** | Authentication required |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

