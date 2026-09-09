# mudbase.RoleElevationApi

All URIs are relative to *https://cloud.mudbase.dev*

Method | HTTP request | Description
------------- | ------------- | -------------
[**approve_role_elevation**](RoleElevationApi.md#approve_role_elevation) | **POST** /api/orgs/{orgId}/role-elevation/{requestId}/approve | Approve/reject role elevation request (admin only)
[**get_pending_role_elevation_requests**](RoleElevationApi.md#get_pending_role_elevation_requests) | **GET** /api/orgs/{orgId}/role-elevation/pending | Get pending role elevation requests (admin only)
[**get_role_elevation_status**](RoleElevationApi.md#get_role_elevation_status) | **GET** /api/projects/{projectId}/role-elevation/status | Get role elevation status
[**request_role_elevation**](RoleElevationApi.md#request_role_elevation) | **POST** /api/projects/{projectId}/role-elevation/request | Request role elevation
[**upload_verification_documents**](RoleElevationApi.md#upload_verification_documents) | **POST** /api/projects/{projectId}/role-elevation/documents | Upload verification documents


# **approve_role_elevation**
> ApproveRoleElevation200Response approve_role_elevation(org_id, request_id, approve_role_elevation_request)

Approve/reject role elevation request (admin only)

Admin approves or rejects a role elevation request

### Example

* Bearer (JWT) Authentication (OrgBearerAuth):
* Bearer (JWT) Authentication (ProjectBearerAuth):

```python
import mudbase
from mudbase.models.approve_role_elevation200_response import ApproveRoleElevation200Response
from mudbase.models.approve_role_elevation_request import ApproveRoleElevationRequest
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
    api_instance = mudbase.RoleElevationApi(api_client)
    org_id = 'org_id_example' # str | 
    request_id = 'request_id_example' # str | 
    approve_role_elevation_request = {"approved":true,"reason":"All requirements met"} # ApproveRoleElevationRequest | 

    try:
        # Approve/reject role elevation request (admin only)
        api_response = api_instance.approve_role_elevation(org_id, request_id, approve_role_elevation_request)
        print("The response of RoleElevationApi->approve_role_elevation:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling RoleElevationApi->approve_role_elevation: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**|  | 
 **request_id** | **str**|  | 
 **approve_role_elevation_request** | [**ApproveRoleElevationRequest**](ApproveRoleElevationRequest.md)|  | 

### Return type

[**ApproveRoleElevation200Response**](ApproveRoleElevation200Response.md)

### Authorization

[OrgBearerAuth](../README.md#OrgBearerAuth), [ProjectBearerAuth](../README.md#ProjectBearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Request approved/rejected |  -  |
**400** | Requirements not met |  -  |
**403** | Insufficient permissions |  -  |
**404** | Request not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_pending_role_elevation_requests**
> GetPendingRoleElevationRequests200Response get_pending_role_elevation_requests(org_id, status=status, page=page, limit=limit)

Get pending role elevation requests (admin only)

Get all pending role elevation requests requiring admin approval

### Example

* Bearer (JWT) Authentication (OrgBearerAuth):
* Bearer (JWT) Authentication (ProjectBearerAuth):

```python
import mudbase
from mudbase.models.get_pending_role_elevation_requests200_response import GetPendingRoleElevationRequests200Response
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
    api_instance = mudbase.RoleElevationApi(api_client)
    org_id = 'org_id_example' # str | 
    status = pending # str |  (optional) (default to pending)
    page = 1 # int |  (optional) (default to 1)
    limit = 50 # int |  (optional) (default to 50)

    try:
        # Get pending role elevation requests (admin only)
        api_response = api_instance.get_pending_role_elevation_requests(org_id, status=status, page=page, limit=limit)
        print("The response of RoleElevationApi->get_pending_role_elevation_requests:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling RoleElevationApi->get_pending_role_elevation_requests: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**|  | 
 **status** | **str**|  | [optional] [default to pending]
 **page** | **int**|  | [optional] [default to 1]
 **limit** | **int**|  | [optional] [default to 50]

### Return type

[**GetPendingRoleElevationRequests200Response**](GetPendingRoleElevationRequests200Response.md)

### Authorization

[OrgBearerAuth](../README.md#OrgBearerAuth), [ProjectBearerAuth](../README.md#ProjectBearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | List of pending requests |  -  |
**403** | Insufficient permissions |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_role_elevation_status**
> GetRoleElevationStatus200Response get_role_elevation_status(project_id, role_slug=role_slug)

Get role elevation status

Get status of pending role elevation requests for current user

### Example

* Bearer (JWT) Authentication (OrgBearerAuth):
* Bearer (JWT) Authentication (ProjectBearerAuth):

```python
import mudbase
from mudbase.models.get_role_elevation_status200_response import GetRoleElevationStatus200Response
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
    api_instance = mudbase.RoleElevationApi(api_client)
    project_id = 'project_id_example' # str | 
    role_slug = 'role_slug_example' # str |  (optional)

    try:
        # Get role elevation status
        api_response = api_instance.get_role_elevation_status(project_id, role_slug=role_slug)
        print("The response of RoleElevationApi->get_role_elevation_status:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling RoleElevationApi->get_role_elevation_status: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **str**|  | 
 **role_slug** | **str**|  | [optional] 

### Return type

[**GetRoleElevationStatus200Response**](GetRoleElevationStatus200Response.md)

### Authorization

[OrgBearerAuth](../README.md#OrgBearerAuth), [ProjectBearerAuth](../README.md#ProjectBearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | List of role elevation requests |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **request_role_elevation**
> RequestRoleElevation200Response request_role_elevation(project_id, request_role_elevation_request)

Request role elevation

User requests to upgrade to a specific role. May require payment, KYC, or admin approval based on role configuration.

### Example

* Bearer (JWT) Authentication (OrgBearerAuth):
* Bearer (JWT) Authentication (ProjectBearerAuth):

```python
import mudbase
from mudbase.models.request_role_elevation200_response import RequestRoleElevation200Response
from mudbase.models.request_role_elevation_request import RequestRoleElevationRequest
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
    api_instance = mudbase.RoleElevationApi(api_client)
    project_id = 'project_id_example' # str | 
    request_role_elevation_request = {"roleSlug":"seller"} # RequestRoleElevationRequest | 

    try:
        # Request role elevation
        api_response = api_instance.request_role_elevation(project_id, request_role_elevation_request)
        print("The response of RoleElevationApi->request_role_elevation:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling RoleElevationApi->request_role_elevation: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **str**|  | 
 **request_role_elevation_request** | [**RequestRoleElevationRequest**](RequestRoleElevationRequest.md)|  | 

### Return type

[**RequestRoleElevation200Response**](RequestRoleElevation200Response.md)

### Authorization

[OrgBearerAuth](../README.md#OrgBearerAuth), [ProjectBearerAuth](../README.md#ProjectBearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Role elevation request created or auto-approved |  -  |
**400** | Invalid request or already has role |  -  |
**403** | Cannot request role with higher hierarchy |  -  |
**404** | Role not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **upload_verification_documents**
> upload_verification_documents(project_id, upload_verification_documents_request)

Upload verification documents

Upload KYC/verification documents for role elevation

### Example

* Bearer (JWT) Authentication (OrgBearerAuth):
* Bearer (JWT) Authentication (ProjectBearerAuth):

```python
import mudbase
from mudbase.models.upload_verification_documents_request import UploadVerificationDocumentsRequest
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
    api_instance = mudbase.RoleElevationApi(api_client)
    project_id = 'project_id_example' # str | 
    upload_verification_documents_request = {"roleSlug":"seller","documents":[{"type":"id","url":"https://example.com/id.pdf"}]} # UploadVerificationDocumentsRequest | 

    try:
        # Upload verification documents
        api_instance.upload_verification_documents(project_id, upload_verification_documents_request)
    except Exception as e:
        print("Exception when calling RoleElevationApi->upload_verification_documents: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **str**|  | 
 **upload_verification_documents_request** | [**UploadVerificationDocumentsRequest**](UploadVerificationDocumentsRequest.md)|  | 

### Return type

void (empty response body)

### Authorization

[OrgBearerAuth](../README.md#OrgBearerAuth), [ProjectBearerAuth](../README.md#ProjectBearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Documents uploaded successfully |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

