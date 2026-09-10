# mudbase.RealTimeAnalyticsApi

All URIs are relative to *https://cloud.mudbase.dev*

Method | HTTP request | Description
------------- | ------------- | -------------
[**check_user_presence**](RealTimeAnalyticsApi.md#check_user_presence) | **POST** /api/realtime/projects/{projectId}/presence | Check presence status for users
[**get_active_users**](RealTimeAnalyticsApi.md#get_active_users) | **GET** /api/realtime/projects/{projectId}/active-users | Get active users for a project
[**get_event_throughput**](RealTimeAnalyticsApi.md#get_event_throughput) | **GET** /api/realtime/projects/{projectId}/throughput | Get event throughput metrics
[**get_global_analytics**](RealTimeAnalyticsApi.md#get_global_analytics) | **GET** /api/realtime/analytics | Get global real-time analytics
[**get_historical_analytics**](RealTimeAnalyticsApi.md#get_historical_analytics) | **GET** /api/realtime/projects/{projectId}/history | Get historical analytics
[**get_project_analytics**](RealTimeAnalyticsApi.md#get_project_analytics) | **GET** /api/realtime/projects/{projectId}/analytics | Get project real-time analytics


# **check_user_presence**
> CheckUserPresence200Response check_user_presence(project_id, check_user_presence_request)

Check presence status for users

Returns online status for specified user IDs

### Example

* Bearer (JWT) Authentication (OrgBearerAuth):
* Bearer (JWT) Authentication (ProjectBearerAuth):

```python
import mudbase
from mudbase.models.check_user_presence200_response import CheckUserPresence200Response
from mudbase.models.check_user_presence_request import CheckUserPresenceRequest
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
    api_instance = mudbase.RealTimeAnalyticsApi(api_client)
    project_id = 'project_id_example' # str | 
    check_user_presence_request = {"userIds":["685acbe0e129932fbb7a0fc2","685acbe0e129932fbb7a0fc3"]} # CheckUserPresenceRequest | 

    try:
        # Check presence status for users
        api_response = api_instance.check_user_presence(project_id, check_user_presence_request)
        print("The response of RealTimeAnalyticsApi->check_user_presence:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling RealTimeAnalyticsApi->check_user_presence: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **str**|  | 
 **check_user_presence_request** | [**CheckUserPresenceRequest**](CheckUserPresenceRequest.md)|  | 

### Return type

[**CheckUserPresence200Response**](CheckUserPresence200Response.md)

### Authorization

[OrgBearerAuth](../README.md#OrgBearerAuth), [ProjectBearerAuth](../README.md#ProjectBearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Presence status for each user |  -  |
**400** | Bad request |  -  |
**401** | Authentication required |  -  |
**404** | Resource not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_active_users**
> GetActiveUsers200Response get_active_users(project_id)

Get active users for a project

Returns list of currently connected users

### Example

* Bearer (JWT) Authentication (OrgBearerAuth):
* Bearer (JWT) Authentication (ProjectBearerAuth):

```python
import mudbase
from mudbase.models.get_active_users200_response import GetActiveUsers200Response
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
    api_instance = mudbase.RealTimeAnalyticsApi(api_client)
    project_id = 'project_id_example' # str | 

    try:
        # Get active users for a project
        api_response = api_instance.get_active_users(project_id)
        print("The response of RealTimeAnalyticsApi->get_active_users:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling RealTimeAnalyticsApi->get_active_users: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **str**|  | 

### Return type

[**GetActiveUsers200Response**](GetActiveUsers200Response.md)

### Authorization

[OrgBearerAuth](../README.md#OrgBearerAuth), [ProjectBearerAuth](../README.md#ProjectBearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | List of active users |  -  |
**401** | Authentication required |  -  |
**404** | Resource not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_event_throughput**
> GetEventThroughput200Response get_event_throughput(project_id, window=window)

Get event throughput metrics

Returns event throughput for a project

### Example

* Bearer (JWT) Authentication (OrgBearerAuth):
* Bearer (JWT) Authentication (ProjectBearerAuth):

```python
import mudbase
from mudbase.models.get_event_throughput200_response import GetEventThroughput200Response
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
    api_instance = mudbase.RealTimeAnalyticsApi(api_client)
    project_id = 'project_id_example' # str | 
    window = 60000 # int | Time window in milliseconds (optional) (default to 60000)

    try:
        # Get event throughput metrics
        api_response = api_instance.get_event_throughput(project_id, window=window)
        print("The response of RealTimeAnalyticsApi->get_event_throughput:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling RealTimeAnalyticsApi->get_event_throughput: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **str**|  | 
 **window** | **int**| Time window in milliseconds | [optional] [default to 60000]

### Return type

[**GetEventThroughput200Response**](GetEventThroughput200Response.md)

### Authorization

[OrgBearerAuth](../README.md#OrgBearerAuth), [ProjectBearerAuth](../README.md#ProjectBearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Throughput metrics |  -  |
**401** | Authentication required |  -  |
**404** | Resource not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_global_analytics**
> GetGlobalAnalytics200Response get_global_analytics()

Get global real-time analytics

Returns system-wide real-time metrics (admin only)

### Example

* Bearer (JWT) Authentication (OrgBearerAuth):
* Bearer (JWT) Authentication (ProjectBearerAuth):

```python
import mudbase
from mudbase.models.get_global_analytics200_response import GetGlobalAnalytics200Response
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
    api_instance = mudbase.RealTimeAnalyticsApi(api_client)

    try:
        # Get global real-time analytics
        api_response = api_instance.get_global_analytics()
        print("The response of RealTimeAnalyticsApi->get_global_analytics:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling RealTimeAnalyticsApi->get_global_analytics: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

[**GetGlobalAnalytics200Response**](GetGlobalAnalytics200Response.md)

### Authorization

[OrgBearerAuth](../README.md#OrgBearerAuth), [ProjectBearerAuth](../README.md#ProjectBearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Global analytics data |  -  |
**401** | Authentication required |  -  |
**403** | Access denied |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_historical_analytics**
> GetHistoricalAnalytics200Response get_historical_analytics(project_id, period=period)

Get historical analytics

Returns historical analytics for charting

### Example

* Bearer (JWT) Authentication (OrgBearerAuth):
* Bearer (JWT) Authentication (ProjectBearerAuth):

```python
import mudbase
from mudbase.models.get_historical_analytics200_response import GetHistoricalAnalytics200Response
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
    api_instance = mudbase.RealTimeAnalyticsApi(api_client)
    project_id = 'project_id_example' # str | 
    period = hour # str | Time period for historical data (optional) (default to hour)

    try:
        # Get historical analytics
        api_response = api_instance.get_historical_analytics(project_id, period=period)
        print("The response of RealTimeAnalyticsApi->get_historical_analytics:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling RealTimeAnalyticsApi->get_historical_analytics: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **str**|  | 
 **period** | **str**| Time period for historical data | [optional] [default to hour]

### Return type

[**GetHistoricalAnalytics200Response**](GetHistoricalAnalytics200Response.md)

### Authorization

[OrgBearerAuth](../README.md#OrgBearerAuth), [ProjectBearerAuth](../README.md#ProjectBearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Historical analytics data |  -  |
**400** | Bad request |  -  |
**401** | Authentication required |  -  |
**404** | Resource not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_project_analytics**
> GetProjectAnalytics200Response get_project_analytics(project_id)

Get project real-time analytics

Returns real-time metrics for a specific project (active connections, events, etc.)

### Example

* Bearer (JWT) Authentication (OrgBearerAuth):
* Bearer (JWT) Authentication (ProjectBearerAuth):

```python
import mudbase
from mudbase.models.get_project_analytics200_response import GetProjectAnalytics200Response
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
    api_instance = mudbase.RealTimeAnalyticsApi(api_client)
    project_id = '685ad30be129932fbb7a1047' # str | 

    try:
        # Get project real-time analytics
        api_response = api_instance.get_project_analytics(project_id)
        print("The response of RealTimeAnalyticsApi->get_project_analytics:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling RealTimeAnalyticsApi->get_project_analytics: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **str**|  | 

### Return type

[**GetProjectAnalytics200Response**](GetProjectAnalytics200Response.md)

### Authorization

[OrgBearerAuth](../README.md#OrgBearerAuth), [ProjectBearerAuth](../README.md#ProjectBearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Project analytics data |  -  |
**401** | Authentication required |  -  |
**404** | Resource not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

