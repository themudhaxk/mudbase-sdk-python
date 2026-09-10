# mudbase.MultiRoleFeatureApi

All URIs are relative to *https://cloud.mudbase.dev*

Method | HTTP request | Description
------------- | ------------- | -------------
[**add_custom_role**](MultiRoleFeatureApi.md#add_custom_role) | **POST** /api/projects/{projectId}/multi-role/roles | Add custom role
[**apply_role_feature_preset**](MultiRoleFeatureApi.md#apply_role_feature_preset) | **POST** /api/projects/{projectId}/multi-role/roles/{roleSlug}/apply-preset | Apply Admin / User / Viewer feature permission preset
[**get_available_roles**](MultiRoleFeatureApi.md#get_available_roles) | **GET** /api/projects/{projectId}/multi-role/roles/available | Get available roles for signup
[**get_multi_role_config**](MultiRoleFeatureApi.md#get_multi_role_config) | **GET** /api/projects/{projectId}/multi-role | Get multi-role feature configuration
[**get_permissions_matrix**](MultiRoleFeatureApi.md#get_permissions_matrix) | **GET** /api/projects/{projectId}/permissions-matrix | Get permissions matrix (collections + featurePermissions)
[**oauth_signup_with_role**](MultiRoleFeatureApi.md#oauth_signup_with_role) | **GET** /api/auth/oauth/signup/{role}/{provider}/{projectId} | OAuth signup with specific role
[**register_with_role**](MultiRoleFeatureApi.md#register_with_role) | **POST** /api/auth/local/signup/{role} | Register user with specific role (Local Auth)
[**simulate_app_permissions**](MultiRoleFeatureApi.md#simulate_app_permissions) | **POST** /api/projects/{projectId}/multi-role/simulate-permissions | Simulate app-role feature permission for a path
[**toggle_role**](MultiRoleFeatureApi.md#toggle_role) | **PATCH** /api/projects/{projectId}/multi-role/roles/{roleSlug}/toggle | Toggle role on/off
[**update_collection_permissions**](MultiRoleFeatureApi.md#update_collection_permissions) | **PATCH** /api/projects/{projectId}/multi-role/roles/{roleSlug}/collections/{collectionId}/permissions | Update collection permissions for a role
[**update_multi_role_settings**](MultiRoleFeatureApi.md#update_multi_role_settings) | **PATCH** /api/projects/{projectId}/multi-role/settings | Update multi-role feature settings
[**update_project_role**](MultiRoleFeatureApi.md#update_project_role) | **PATCH** /api/projects/{projectId}/multi-role/roles/{roleSlug} | Update role configuration


# **add_custom_role**
> ApplyRoleFeaturePreset200Response add_custom_role(project_id, add_custom_role_request)

Add custom role

Add a custom role to a project with specific permissions and signup endpoint.
Optional **`featurePermissions`** must align with app JWT gates — see `components/schemas/AppRoleFeaturePermissions`
and `services/appRoleFeatureMap.js`.
Accepts: OrgBearerAuth (for admin users), ProjectBearerAuth (JWT for authenticated users), or ApiKeyAuth (X-API-Key for programmatic access). Both ProjectBearerAuth and ApiKeyAuth are fully implemented.


### Example

* Bearer (JWT) Authentication (OrgBearerAuth):
* Bearer (JWT) Authentication (ProjectBearerAuth):

```python
import mudbase
from mudbase.models.add_custom_role_request import AddCustomRoleRequest
from mudbase.models.apply_role_feature_preset200_response import ApplyRoleFeaturePreset200Response
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
    api_instance = mudbase.MultiRoleFeatureApi(api_client)
    project_id = '65f1a2b3c4d5e6f7a8b9c0d1' # str | 
    add_custom_role_request = {"slug":"seller","name":"Seller","description":"Seller role with CRUD on seller-owned collections","signupEndpoint":"seller","requiresApproval":false,"requiresPayment":false,"requiresKYC":false,"metadata":{"notes":"Example role for API integration tests"},"defaultPermissions":[{"resource":"project","actions":["read"]},{"resource":"data","actions":["read","create"]}],"collectionPermissions":{"listings":["create","read","update","delete"],"orders":{"actions":["create","read"],"conditions":{"status":"active"}}},"featurePermissions":{"messaging":{"email":true,"sms":true,"push":true,"history":true,"stats":true},"integration":{"read":true,"create":true,"update":true,"delete":false,"execute":true,"test":true,"export":true,"read_usage":true},"functions":{"create":true,"read":true,"update":true,"delete":false,"execute":true,"simulate":true},"data":{"create":true,"read":true,"update":true,"delete":false},"search":{"query":true,"suggestions":true,"read_analytics":true},"usage":{"read":true},"storage":{"read":true,"create":true,"update":true,"delete":false,"upload":true},"chat":{"read":true,"create":true,"update":true,"delete":false},"realtime":{"read_analytics":true,"read_active_users":true,"presence":true,"read_throughput":true,"read_history":true},"roleElevation":{"request":true,"status":true,"documents":true},"webhooks":{"config_read":true,"config_update":true,"test_transformation":true}}} # AddCustomRoleRequest | 

    try:
        # Add custom role
        api_response = api_instance.add_custom_role(project_id, add_custom_role_request)
        print("The response of MultiRoleFeatureApi->add_custom_role:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling MultiRoleFeatureApi->add_custom_role: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **str**|  | 
 **add_custom_role_request** | [**AddCustomRoleRequest**](AddCustomRoleRequest.md)|  | 

### Return type

[**ApplyRoleFeaturePreset200Response**](ApplyRoleFeaturePreset200Response.md)

### Authorization

[OrgBearerAuth](../README.md#OrgBearerAuth), [ProjectBearerAuth](../README.md#ProjectBearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | Custom role added |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **apply_role_feature_preset**
> ApplyRoleFeaturePreset200Response apply_role_feature_preset(project_id, role_slug, apply_role_feature_preset_request)

Apply Admin / User / Viewer feature permission preset

Sets `featurePermissions` on the role from a bundled preset (`admin`, `user`, `viewer`).
Does not change collection CRUD or `dataScope`; use collection permission APIs for those.


### Example

* Bearer (JWT) Authentication (OrgBearerAuth):
* Bearer (JWT) Authentication (ProjectBearerAuth):

```python
import mudbase
from mudbase.models.apply_role_feature_preset200_response import ApplyRoleFeaturePreset200Response
from mudbase.models.apply_role_feature_preset_request import ApplyRoleFeaturePresetRequest
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
    api_instance = mudbase.MultiRoleFeatureApi(api_client)
    project_id = 'project_id_example' # str | 
    role_slug = 'role_slug_example' # str | 
    apply_role_feature_preset_request = {"preset":"admin"} # ApplyRoleFeaturePresetRequest | 

    try:
        # Apply Admin / User / Viewer feature permission preset
        api_response = api_instance.apply_role_feature_preset(project_id, role_slug, apply_role_feature_preset_request)
        print("The response of MultiRoleFeatureApi->apply_role_feature_preset:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling MultiRoleFeatureApi->apply_role_feature_preset: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **str**|  | 
 **role_slug** | **str**|  | 
 **apply_role_feature_preset_request** | [**ApplyRoleFeaturePresetRequest**](ApplyRoleFeaturePresetRequest.md)|  | 

### Return type

[**ApplyRoleFeaturePreset200Response**](ApplyRoleFeaturePreset200Response.md)

### Authorization

[OrgBearerAuth](../README.md#OrgBearerAuth), [ProjectBearerAuth](../README.md#ProjectBearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Preset applied |  -  |
**400** | Bad request |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_available_roles**
> GetAvailableRoles200Response get_available_roles(project_id)

Get available roles for signup

Get all available roles for user signup in a project.
Accepts: OrgBearerAuth (for admin users), ProjectBearerAuth (JWT for authenticated users), or ApiKeyAuth (X-API-Key for programmatic access). Both ProjectBearerAuth and ApiKeyAuth are fully implemented.


### Example

* Bearer (JWT) Authentication (OrgBearerAuth):
* Bearer (JWT) Authentication (ProjectBearerAuth):

```python
import mudbase
from mudbase.models.get_available_roles200_response import GetAvailableRoles200Response
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
    api_instance = mudbase.MultiRoleFeatureApi(api_client)
    project_id = '65f1a2b3c4d5e6f7a8b9c0d1' # str | 

    try:
        # Get available roles for signup
        api_response = api_instance.get_available_roles(project_id)
        print("The response of MultiRoleFeatureApi->get_available_roles:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling MultiRoleFeatureApi->get_available_roles: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **str**|  | 

### Return type

[**GetAvailableRoles200Response**](GetAvailableRoles200Response.md)

### Authorization

[OrgBearerAuth](../README.md#OrgBearerAuth), [ProjectBearerAuth](../README.md#ProjectBearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | List of available roles |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_multi_role_config**
> GetMultiRoleConfig200Response get_multi_role_config(project_id)

Get multi-role feature configuration

Returns project app roles (default one editable `customer` starter until you add more) and settings

### Example

* Bearer (JWT) Authentication (OrgBearerAuth):
* Bearer (JWT) Authentication (ProjectBearerAuth):

```python
import mudbase
from mudbase.models.get_multi_role_config200_response import GetMultiRoleConfig200Response
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
    api_instance = mudbase.MultiRoleFeatureApi(api_client)
    project_id = '65f1a2b3c4d5e6f7a8b9c0d1' # str | 

    try:
        # Get multi-role feature configuration
        api_response = api_instance.get_multi_role_config(project_id)
        print("The response of MultiRoleFeatureApi->get_multi_role_config:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling MultiRoleFeatureApi->get_multi_role_config: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **str**|  | 

### Return type

[**GetMultiRoleConfig200Response**](GetMultiRoleConfig200Response.md)

### Authorization

[OrgBearerAuth](../README.md#OrgBearerAuth), [ProjectBearerAuth](../README.md#ProjectBearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Multi-role configuration |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_permissions_matrix**
> GetPermissionsMatrix200Response get_permissions_matrix(project_id)

Get permissions matrix (collections + featurePermissions)

Dashboard helper: per-collection permission rows (role actions, `dataScope`, conditions) and a per-role
`featurePermissions` snapshot used by app-role feature gates (messaging, integrations, storage, etc.).


### Example

* Bearer (JWT) Authentication (OrgBearerAuth):
* Bearer (JWT) Authentication (ProjectBearerAuth):

```python
import mudbase
from mudbase.models.get_permissions_matrix200_response import GetPermissionsMatrix200Response
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
    api_instance = mudbase.MultiRoleFeatureApi(api_client)
    project_id = '65f1a2b3c4d5e6f7a8b9c0d1' # str | 

    try:
        # Get permissions matrix (collections + featurePermissions)
        api_response = api_instance.get_permissions_matrix(project_id)
        print("The response of MultiRoleFeatureApi->get_permissions_matrix:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling MultiRoleFeatureApi->get_permissions_matrix: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **str**|  | 

### Return type

[**GetPermissionsMatrix200Response**](GetPermissionsMatrix200Response.md)

### Authorization

[OrgBearerAuth](../README.md#OrgBearerAuth), [ProjectBearerAuth](../README.md#ProjectBearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Matrix payload |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **oauth_signup_with_role**
> oauth_signup_with_role(role, provider, project_id, redirect_url=redirect_url)

OAuth signup with specific role

Public endpoint that initiates OAuth signup flow with a specific role assigned during registration.
The OAuth provider must be configured and enabled for the project first.
The role must be available for signup in the project's multi-role configuration.
After successful OAuth authentication, the user will be created with the specified role.
No authentication required - this is a public signup endpoint.


### Example


```python
import mudbase
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
    api_instance = mudbase.MultiRoleFeatureApi(api_client)
    role = 'customer' # str | Path segment must match the role's `signupEndpoint` (default `customer`; use each role's configured endpoint).
    provider = 'google' # str | 
    project_id = '65f1a2b3c4d5e6f7a8b9c0d1' # str | 
    redirect_url = 'https://client.app/auth/callback' # str | The URL to redirect to after authentication (optional)

    try:
        # OAuth signup with specific role
        api_instance.oauth_signup_with_role(role, provider, project_id, redirect_url=redirect_url)
    except Exception as e:
        print("Exception when calling MultiRoleFeatureApi->oauth_signup_with_role: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **role** | **str**| Path segment must match the role&#39;s &#x60;signupEndpoint&#x60; (default &#x60;customer&#x60;; use each role&#39;s configured endpoint). | 
 **provider** | **str**|  | 
 **project_id** | **str**|  | 
 **redirect_url** | **str**| The URL to redirect to after authentication | [optional] 

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**302** | Redirects to OAuth provider&#39;s consent screen |  * Location - OAuth provider authorization URL <br>  |
**400** | OAuth provider not configured, role not found, or validation error |  -  |
**404** | Project not found |  -  |
**500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **register_with_role**
> RegisterWithRole201Response register_with_role(role, register_with_role_request)

Register user with specific role (Local Auth)

Public endpoint for user registration with a specific role. The path segment must match a role's `signupEndpoint` (default starter is `customer`; add more roles via multi-role API).
No authentication required - this is a public signup endpoint.


### Example


```python
import mudbase
from mudbase.models.register_with_role201_response import RegisterWithRole201Response
from mudbase.models.register_with_role_request import RegisterWithRoleRequest
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
    api_instance = mudbase.MultiRoleFeatureApi(api_client)
    role = 'customer' # str | Must match the role's `signupEndpoint` (default `customer`; other values for roles you add).
    register_with_role_request = {"email":"customer@example.com","password":"SecurePass123!","firstName":"Jane","lastName":"Doe","projectId":"65f1a2b3c4d5e6f7a8b9c0d1","agreedToTerms":true} # RegisterWithRoleRequest | 

    try:
        # Register user with specific role (Local Auth)
        api_response = api_instance.register_with_role(role, register_with_role_request)
        print("The response of MultiRoleFeatureApi->register_with_role:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling MultiRoleFeatureApi->register_with_role: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **role** | **str**| Must match the role&#39;s &#x60;signupEndpoint&#x60; (default &#x60;customer&#x60;; other values for roles you add). | 
 **register_with_role_request** | [**RegisterWithRoleRequest**](RegisterWithRoleRequest.md)|  | 

### Return type

[**RegisterWithRole201Response**](RegisterWithRole201Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | Registration successful. Two response shapes depending on the project&#39;s &#x60;requireEmailVerification&#x60; setting - see &#x60;requireVerification&#x60; to distinguish them; &#x60;token&#x60;/&#x60;refreshToken&#x60;/&#x60;expiresIn&#x60; are only present when a session was issued immediately. |  -  |
**400** | Validation failed, or a user with this email already exists for the project |  -  |
**403** | Role requires approval, payment, or KYC before it can be self-assigned |  -  |
**404** | Role not found or not enabled |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **simulate_app_permissions**
> SimulateAppPermissions200Response simulate_app_permissions(project_id, simulate_app_permissions_request)

Simulate app-role feature permission for a path

Dashboard-only. Given an app role slug and either an OpenAPI `operationId` **or** HTTP method + pathname,
returns whether the role's `featurePermissions` would allow the operation for paths that have a feature gate.
Unmapped paths or unknown operation IDs return `allowed: true` with reason `no_feature_gate_for_path` or
`no_feature_gate_for_operation_id`.


### Example

* Bearer (JWT) Authentication (OrgBearerAuth):
* Bearer (JWT) Authentication (ProjectBearerAuth):

```python
import mudbase
from mudbase.models.simulate_app_permissions200_response import SimulateAppPermissions200Response
from mudbase.models.simulate_app_permissions_request import SimulateAppPermissionsRequest
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
    api_instance = mudbase.MultiRoleFeatureApi(api_client)
    project_id = 'project_id_example' # str | 
    simulate_app_permissions_request = {"role":"customer","method":"POST","pathname":"/api/messaging/projects/65f1a2b3c4d5e6f7a8b9c0d1/messaging/email"} # SimulateAppPermissionsRequest | 

    try:
        # Simulate app-role feature permission for a path
        api_response = api_instance.simulate_app_permissions(project_id, simulate_app_permissions_request)
        print("The response of MultiRoleFeatureApi->simulate_app_permissions:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling MultiRoleFeatureApi->simulate_app_permissions: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **str**|  | 
 **simulate_app_permissions_request** | [**SimulateAppPermissionsRequest**](SimulateAppPermissionsRequest.md)|  | 

### Return type

[**SimulateAppPermissions200Response**](SimulateAppPermissions200Response.md)

### Authorization

[OrgBearerAuth](../README.md#OrgBearerAuth), [ProjectBearerAuth](../README.md#ProjectBearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Simulation result |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **toggle_role**
> ApplyRoleFeaturePreset200Response toggle_role(project_id, role_slug, toggle_role_request)

Toggle role on/off

### Example

* Bearer (JWT) Authentication (OrgBearerAuth):
* Bearer (JWT) Authentication (ProjectBearerAuth):

```python
import mudbase
from mudbase.models.apply_role_feature_preset200_response import ApplyRoleFeaturePreset200Response
from mudbase.models.toggle_role_request import ToggleRoleRequest
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
    api_instance = mudbase.MultiRoleFeatureApi(api_client)
    project_id = '65f1a2b3c4d5e6f7a8b9c0d1' # str | 
    role_slug = 'customer' # str | Role slug to toggle (e.g. starter `customer` or a role you added).
    toggle_role_request = {"isEnabled":true} # ToggleRoleRequest | 

    try:
        # Toggle role on/off
        api_response = api_instance.toggle_role(project_id, role_slug, toggle_role_request)
        print("The response of MultiRoleFeatureApi->toggle_role:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling MultiRoleFeatureApi->toggle_role: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **str**|  | 
 **role_slug** | **str**| Role slug to toggle (e.g. starter &#x60;customer&#x60; or a role you added). | 
 **toggle_role_request** | [**ToggleRoleRequest**](ToggleRoleRequest.md)|  | 

### Return type

[**ApplyRoleFeaturePreset200Response**](ApplyRoleFeaturePreset200Response.md)

### Authorization

[OrgBearerAuth](../README.md#OrgBearerAuth), [ProjectBearerAuth](../README.md#ProjectBearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Role toggled |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_collection_permissions**
> ApplyRoleFeaturePreset200Response update_collection_permissions(project_id, role_slug, collection_id, update_collection_permissions_request)

Update collection permissions for a role

Update collection-specific permissions for a role in a project.
Accepts: OrgBearerAuth (for admin users), ProjectBearerAuth (JWT for authenticated users), or ApiKeyAuth (X-API-Key for programmatic access). Both ProjectBearerAuth and ApiKeyAuth are fully implemented.


### Example

* Bearer (JWT) Authentication (OrgBearerAuth):
* Bearer (JWT) Authentication (ProjectBearerAuth):

```python
import mudbase
from mudbase.models.apply_role_feature_preset200_response import ApplyRoleFeaturePreset200Response
from mudbase.models.update_collection_permissions_request import UpdateCollectionPermissionsRequest
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
    api_instance = mudbase.MultiRoleFeatureApi(api_client)
    project_id = '65f1a2b3c4d5e6f7a8b9c0d1' # str | 
    role_slug = 'customer' # str | Role slug (e.g. starter `customer` or a role you added).
    collection_id = '696ba6e4f4a9422ac4be4f74' # str | 
    update_collection_permissions_request = {"actions":["create","read","update","delete"],"conditions":{"status":"active"},"dataScope":"own"} # UpdateCollectionPermissionsRequest | 

    try:
        # Update collection permissions for a role
        api_response = api_instance.update_collection_permissions(project_id, role_slug, collection_id, update_collection_permissions_request)
        print("The response of MultiRoleFeatureApi->update_collection_permissions:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling MultiRoleFeatureApi->update_collection_permissions: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **str**|  | 
 **role_slug** | **str**| Role slug (e.g. starter &#x60;customer&#x60; or a role you added). | 
 **collection_id** | **str**|  | 
 **update_collection_permissions_request** | [**UpdateCollectionPermissionsRequest**](UpdateCollectionPermissionsRequest.md)|  | 

### Return type

[**ApplyRoleFeaturePreset200Response**](ApplyRoleFeaturePreset200Response.md)

### Authorization

[OrgBearerAuth](../README.md#OrgBearerAuth), [ProjectBearerAuth](../README.md#ProjectBearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Collection permissions updated |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_multi_role_settings**
> UpdateMultiRoleSettings200Response update_multi_role_settings(project_id, update_multi_role_settings_request)

Update multi-role feature settings

Update multi-role feature settings for a project: enable/disable the feature, set which app role is the default at signup, and tune `settings` (`allowMultipleRoles`, `requireRoleSelection`, `autoAssignDefault`).
This endpoint does **not** edit role definitions or permissions — use `POST/PATCH .../multi-role/roles` for that (same shape as **Add custom role**).
Accepts: OrgBearerAuth (for admin users), ProjectBearerAuth (JWT for authenticated users), or ApiKeyAuth (X-API-Key for programmatic access). Both ProjectBearerAuth and ApiKeyAuth are fully implemented.


### Example

* Bearer (JWT) Authentication (OrgBearerAuth):
* Bearer (JWT) Authentication (ProjectBearerAuth):

```python
import mudbase
from mudbase.models.update_multi_role_settings200_response import UpdateMultiRoleSettings200Response
from mudbase.models.update_multi_role_settings_request import UpdateMultiRoleSettingsRequest
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
    api_instance = mudbase.MultiRoleFeatureApi(api_client)
    project_id = '65f1a2b3c4d5e6f7a8b9c0d1' # str | 
    update_multi_role_settings_request = {"isEnabled":true,"defaultRole":"customer","settings":{"allowMultipleRoles":false,"requireRoleSelection":false,"autoAssignDefault":true,"dataOwnerField":"createdBy"}} # UpdateMultiRoleSettingsRequest | 

    try:
        # Update multi-role feature settings
        api_response = api_instance.update_multi_role_settings(project_id, update_multi_role_settings_request)
        print("The response of MultiRoleFeatureApi->update_multi_role_settings:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling MultiRoleFeatureApi->update_multi_role_settings: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **str**|  | 
 **update_multi_role_settings_request** | [**UpdateMultiRoleSettingsRequest**](UpdateMultiRoleSettingsRequest.md)|  | 

### Return type

[**UpdateMultiRoleSettings200Response**](UpdateMultiRoleSettings200Response.md)

### Authorization

[OrgBearerAuth](../README.md#OrgBearerAuth), [ProjectBearerAuth](../README.md#ProjectBearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Settings updated |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_project_role**
> ApplyRoleFeaturePreset200Response update_project_role(project_id, role_slug, update_project_role_request)

Update role configuration

Partial update of an app role. **`featurePermissions`** keys must match the app-role gate map
(`services/appRoleFeatureMap.js`); schema: `components/schemas/AppRoleFeaturePermissions`.


### Example

* Bearer (JWT) Authentication (OrgBearerAuth):
* Bearer (JWT) Authentication (ProjectBearerAuth):

```python
import mudbase
from mudbase.models.apply_role_feature_preset200_response import ApplyRoleFeaturePreset200Response
from mudbase.models.update_project_role_request import UpdateProjectRoleRequest
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
    api_instance = mudbase.MultiRoleFeatureApi(api_client)
    project_id = '65f1a2b3c4d5e6f7a8b9c0d1' # str | 
    role_slug = 'customer' # str | Role slug to update (e.g. starter `customer` or a role you added).
    update_project_role_request = {"name":"App user","description":"End users of the app","signupEndpoint":"customer","requiresApproval":false,"requiresPayment":false,"requiresKYC":false,"collectionPermissions":{"posts":["create","read","update","delete"]},"featurePermissions":{"messaging":{"email":true,"sms":false,"push":false},"integration":{"read":true,"execute":true}}} # UpdateProjectRoleRequest | Same fields as **Add custom role** — send only fields you want to change. `defaultPermissions` / `collectionPermissions` are normalized the same way as on create. **`featurePermissions`:** `components/schemas/AppRoleFeaturePermissions` (aligned with `services/appRoleFeatureMap.js`). 

    try:
        # Update role configuration
        api_response = api_instance.update_project_role(project_id, role_slug, update_project_role_request)
        print("The response of MultiRoleFeatureApi->update_project_role:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling MultiRoleFeatureApi->update_project_role: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **str**|  | 
 **role_slug** | **str**| Role slug to update (e.g. starter &#x60;customer&#x60; or a role you added). | 
 **update_project_role_request** | [**UpdateProjectRoleRequest**](UpdateProjectRoleRequest.md)| Same fields as **Add custom role** — send only fields you want to change. &#x60;defaultPermissions&#x60; / &#x60;collectionPermissions&#x60; are normalized the same way as on create. **&#x60;featurePermissions&#x60;:** &#x60;components/schemas/AppRoleFeaturePermissions&#x60; (aligned with &#x60;services/appRoleFeatureMap.js&#x60;).  | 

### Return type

[**ApplyRoleFeaturePreset200Response**](ApplyRoleFeaturePreset200Response.md)

### Authorization

[OrgBearerAuth](../README.md#OrgBearerAuth), [ProjectBearerAuth](../README.md#ProjectBearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Role updated |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

