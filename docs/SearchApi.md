# mudbase.SearchApi

All URIs are relative to *https://cloud.mudbase.dev*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_search_analytics**](SearchApi.md#get_search_analytics) | **GET** /api/search/projects/{projectId}/search/analytics | Get search analytics
[**get_search_suggestions**](SearchApi.md#get_search_suggestions) | **GET** /api/search/projects/{projectId}/search/suggestions | Get search suggestions
[**search_data**](SearchApi.md#search_data) | **GET** /api/search/projects/{projectId}/search | Full-text search


# **get_search_analytics**
> GetSearchAnalytics200Response get_search_analytics(project_id, timeframe=timeframe)

Get search analytics

Get search analytics including top queries, search volume, and performance metrics.
Accepts: OrgBearerAuth (for admin users), ProjectBearerAuth (JWT for authenticated users), or ApiKeyAuth (X-API-Key for programmatic access). Both ProjectBearerAuth and ApiKeyAuth are fully implemented.


### Example

* Bearer (JWT) Authentication (OrgBearerAuth):
* Bearer (JWT) Authentication (ProjectBearerAuth):

```python
import mudbase
from mudbase.models.get_search_analytics200_response import GetSearchAnalytics200Response
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
    api_instance = mudbase.SearchApi(api_client)
    project_id = '685ad30be129932fbb7a1047' # str | 
    timeframe = 7d # str |  (optional) (default to 7d)

    try:
        # Get search analytics
        api_response = api_instance.get_search_analytics(project_id, timeframe=timeframe)
        print("The response of SearchApi->get_search_analytics:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling SearchApi->get_search_analytics: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **str**|  | 
 **timeframe** | **str**|  | [optional] [default to 7d]

### Return type

[**GetSearchAnalytics200Response**](GetSearchAnalytics200Response.md)

### Authorization

[OrgBearerAuth](../README.md#OrgBearerAuth), [ProjectBearerAuth](../README.md#ProjectBearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Search analytics |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_search_suggestions**
> GetSearchSuggestions200Response get_search_suggestions(project_id, q, limit=limit)

Get search suggestions

Get search query suggestions based on partial input.
Accepts: OrgBearerAuth (for admin users), ProjectBearerAuth (JWT for authenticated users), or ApiKeyAuth (X-API-Key for programmatic access). Both ProjectBearerAuth and ApiKeyAuth are fully implemented.


### Example

* Bearer (JWT) Authentication (OrgBearerAuth):
* Bearer (JWT) Authentication (ProjectBearerAuth):

```python
import mudbase
from mudbase.models.get_search_suggestions200_response import GetSearchSuggestions200Response
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
    api_instance = mudbase.SearchApi(api_client)
    project_id = '685ad30be129932fbb7a1047' # str | 
    q = 'q_example' # str | 
    limit = 10 # int |  (optional) (default to 10)

    try:
        # Get search suggestions
        api_response = api_instance.get_search_suggestions(project_id, q, limit=limit)
        print("The response of SearchApi->get_search_suggestions:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling SearchApi->get_search_suggestions: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **str**|  | 
 **q** | **str**|  | 
 **limit** | **int**|  | [optional] [default to 10]

### Return type

[**GetSearchSuggestions200Response**](GetSearchSuggestions200Response.md)

### Authorization

[OrgBearerAuth](../README.md#OrgBearerAuth), [ProjectBearerAuth](../README.md#ProjectBearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Search suggestions |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **search_data**
> SearchResponse search_data(project_id, q, collections=collections, fields=fields, limit=limit, page=page)

Full-text search

Perform full-text search across collections in a project.
Accepts: OrgBearerAuth (for admin users), ProjectBearerAuth (JWT for authenticated users), or ApiKeyAuth (X-API-Key for programmatic access). Both ProjectBearerAuth and ApiKeyAuth are fully implemented.


### Example

* Bearer (JWT) Authentication (OrgBearerAuth):
* Bearer (JWT) Authentication (ProjectBearerAuth):

```python
import mudbase
from mudbase.models.search_response import SearchResponse
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
    api_instance = mudbase.SearchApi(api_client)
    project_id = 'project_id_example' # str | 
    q = 'q_example' # str | 
    collections = 'collections_example' # str |  (optional)
    fields = 'fields_example' # str |  (optional)
    limit = 20 # int |  (optional) (default to 20)
    page = 1 # int |  (optional) (default to 1)

    try:
        # Full-text search
        api_response = api_instance.search_data(project_id, q, collections=collections, fields=fields, limit=limit, page=page)
        print("The response of SearchApi->search_data:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling SearchApi->search_data: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **str**|  | 
 **q** | **str**|  | 
 **collections** | **str**|  | [optional] 
 **fields** | **str**|  | [optional] 
 **limit** | **int**|  | [optional] [default to 20]
 **page** | **int**|  | [optional] [default to 1]

### Return type

[**SearchResponse**](SearchResponse.md)

### Authorization

[OrgBearerAuth](../README.md#OrgBearerAuth), [ProjectBearerAuth](../README.md#ProjectBearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Search results |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

