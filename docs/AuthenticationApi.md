# mudbase.AuthenticationApi

All URIs are relative to *https://cloud.mudbase.dev*

Method | HTTP request | Description
------------- | ------------- | -------------
[**accept_invite**](AuthenticationApi.md#accept_invite) | **POST** /api/auth/accept-invite | Accept organization invitation
[**confirm_local_password_reset_with_otp**](AuthenticationApi.md#confirm_local_password_reset_with_otp) | **POST** /api/auth/local/password-reset/confirm | Confirm password reset with OTP (project-based)
[**convert_anonymous_account**](AuthenticationApi.md#convert_anonymous_account) | **POST** /api/auth/anonymous/convert | Convert anonymous account to full account
[**create_anonymous_session**](AuthenticationApi.md#create_anonymous_session) | **POST** /api/auth/anonymous | Create anonymous session
[**get_available_o_auth_providers**](AuthenticationApi.md#get_available_o_auth_providers) | **GET** /api/auth/oauth/providers/available | Get all available OAuth providers
[**get_current_session**](AuthenticationApi.md#get_current_session) | **GET** /api/auth/session | Get current session
[**get_local_session**](AuthenticationApi.md#get_local_session) | **GET** /api/auth/local/session | Get current session (project-based)
[**get_org_o_auth_providers**](AuthenticationApi.md#get_org_o_auth_providers) | **GET** /api/auth/oauth-org/providers | Get available OAuth providers for organization-based auth
[**initiate_o_auth**](AuthenticationApi.md#initiate_o_auth) | **GET** /api/auth/oauth/{provider}/{projectId} | Initiate OAuth authentication
[**initiate_org_o_auth**](AuthenticationApi.md#initiate_org_o_auth) | **GET** /api/auth/oauth-org/{provider} | Initiate OAuth authentication for organization
[**login_local_user**](AuthenticationApi.md#login_local_user) | **POST** /api/auth/local/login | Login user (project-based)
[**login_user**](AuthenticationApi.md#login_user) | **POST** /api/auth/login | Login user
[**logout_local_user**](AuthenticationApi.md#logout_local_user) | **POST** /api/auth/local/logout | Logout user (project-based)
[**logout_user**](AuthenticationApi.md#logout_user) | **POST** /api/auth/logout | Logout user
[**oauth_callback**](AuthenticationApi.md#oauth_callback) | **GET** /api/auth/oauth/callback/{provider} | OAuth callback handler (project-based)
[**org_o_auth_callback**](AuthenticationApi.md#org_o_auth_callback) | **GET** /api/auth/oauth-org/callback/{provider} | OAuth callback handler for organization
[**refresh_token**](AuthenticationApi.md#refresh_token) | **POST** /api/auth/refresh | Refresh access token (org and project)
[**register_local_user**](AuthenticationApi.md#register_local_user) | **POST** /api/auth/local/register | Register new user (project-based)
[**register_user**](AuthenticationApi.md#register_user) | **POST** /api/auth/register | Register new user
[**request_local_password_reset**](AuthenticationApi.md#request_local_password_reset) | **POST** /api/auth/local/password-reset | Request password reset (project-based, OTP)
[**request_password_reset**](AuthenticationApi.md#request_password_reset) | **POST** /api/auth/password-reset | Request password reset (organization / platform)
[**resend_verification_auth**](AuthenticationApi.md#resend_verification_auth) | **POST** /api/auth/resend-verification | Resend verification email (no auth)
[**reset_local_password**](AuthenticationApi.md#reset_local_password) | **POST** /api/auth/local/password-reset/{token} | Reset password with token (project-based, legacy)
[**reset_password**](AuthenticationApi.md#reset_password) | **POST** /api/auth/password-reset/{token} | Reset password with token (organization / platform)
[**send_magic_link**](AuthenticationApi.md#send_magic_link) | **POST** /api/auth/magic-link/send | Send magic link
[**send_otp**](AuthenticationApi.md#send_otp) | **POST** /api/auth/otp/send | Send OTP code
[**validate_password_reset_token**](AuthenticationApi.md#validate_password_reset_token) | **POST** /api/auth/password-reset/validate | Validate password reset token
[**verify_email_auth**](AuthenticationApi.md#verify_email_auth) | **POST** /api/auth/verify-email | Verify email address (no auth)
[**verify_magic_link**](AuthenticationApi.md#verify_magic_link) | **POST** /api/auth/magic-link/verify | Verify magic link
[**verify_otp**](AuthenticationApi.md#verify_otp) | **POST** /api/auth/otp/verify | Verify OTP code


# **accept_invite**
> AcceptInvite201Response accept_invite(accept_invite_request)

Accept organization invitation

Accept an organization invitation using the token from the invite email link (e.g. `/invite/{token}?orgId=...`).
Creates a new user with the invited email and adds them to the organization with the invited role.
Returns a JWT and user so the client can log the user in immediately. No authentication required.


### Example


```python
import mudbase
from mudbase.models.accept_invite201_response import AcceptInvite201Response
from mudbase.models.accept_invite_request import AcceptInviteRequest
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
    api_instance = mudbase.AuthenticationApi(api_client)
    accept_invite_request = {"token":"a1b2c3d4e5f6...","password":"SecurePass123!","firstName":"Jane","lastName":"Doe"} # AcceptInviteRequest | 

    try:
        # Accept organization invitation
        api_response = api_instance.accept_invite(accept_invite_request)
        print("The response of AuthenticationApi->accept_invite:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AuthenticationApi->accept_invite: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **accept_invite_request** | [**AcceptInviteRequest**](AcceptInviteRequest.md)|  | 

### Return type

[**AcceptInvite201Response**](AcceptInvite201Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | Invitation accepted; user created and added to organization |  -  |
**400** | Invalid or expired token, or user already exists with this email |  -  |
**404** | Organization not found |  -  |
**500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **confirm_local_password_reset_with_otp**
> MessageResponse confirm_local_password_reset_with_otp(confirm_local_password_reset_with_otp_request)

Confirm password reset with OTP (project-based)

Set new password using the OTP sent to the user's email. Call after
POST /api/auth/local/password-reset with projectId. Rate limited (OTP limit).
If the user's email was not yet verified, it is marked as verified upon successful reset.


### Example


```python
import mudbase
from mudbase.models.confirm_local_password_reset_with_otp_request import ConfirmLocalPasswordResetWithOtpRequest
from mudbase.models.message_response import MessageResponse
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
    api_instance = mudbase.AuthenticationApi(api_client)
    confirm_local_password_reset_with_otp_request = {"email":"user@example.com","projectId":"685ad30be129932fbb7a1047","otp":"123456","newPassword":"NewSecurePass123!"} # ConfirmLocalPasswordResetWithOtpRequest | 

    try:
        # Confirm password reset with OTP (project-based)
        api_response = api_instance.confirm_local_password_reset_with_otp(confirm_local_password_reset_with_otp_request)
        print("The response of AuthenticationApi->confirm_local_password_reset_with_otp:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AuthenticationApi->confirm_local_password_reset_with_otp: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **confirm_local_password_reset_with_otp_request** | [**ConfirmLocalPasswordResetWithOtpRequest**](ConfirmLocalPasswordResetWithOtpRequest.md)|  | 

### Return type

[**MessageResponse**](MessageResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Password reset successful |  -  |
**400** | Invalid or expired OTP, or validation error |  -  |
**404** | Resource not found |  -  |
**429** | Too many attempts (rate limit) |  -  |
**500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **convert_anonymous_account**
> ConvertAnonymousAccount200Response convert_anonymous_account(convert_anonymous_account_request)

Convert anonymous account to full account

Convert an anonymous user session to a full authenticated account. Preserves user data. Requires JWT Bearer token authentication. Both OrgBearerAuth and ProjectBearerAuth are supported (they use the same JWT token format). API keys are not supported for this endpoint.


### Example

* Bearer (JWT) Authentication (OrgBearerAuth):
* Bearer (JWT) Authentication (ProjectBearerAuth):

```python
import mudbase
from mudbase.models.convert_anonymous_account200_response import ConvertAnonymousAccount200Response
from mudbase.models.convert_anonymous_account_request import ConvertAnonymousAccountRequest
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
    api_instance = mudbase.AuthenticationApi(api_client)
    convert_anonymous_account_request = {"email":"user@example.com","password":"SecurePassword123!","firstName":"John","lastName":"Doe"} # ConvertAnonymousAccountRequest | 

    try:
        # Convert anonymous account to full account
        api_response = api_instance.convert_anonymous_account(convert_anonymous_account_request)
        print("The response of AuthenticationApi->convert_anonymous_account:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AuthenticationApi->convert_anonymous_account: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **convert_anonymous_account_request** | [**ConvertAnonymousAccountRequest**](ConvertAnonymousAccountRequest.md)|  | 

### Return type

[**ConvertAnonymousAccount200Response**](ConvertAnonymousAccount200Response.md)

### Authorization

[OrgBearerAuth](../README.md#OrgBearerAuth), [ProjectBearerAuth](../README.md#ProjectBearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Account converted successfully |  -  |
**400** | Bad request |  -  |
**401** | Authentication required |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **create_anonymous_session**
> CreateAnonymousSession200Response create_anonymous_session(create_anonymous_session_request=create_anonymous_session_request)

Create anonymous session

Create an anonymous user session for guest access. Users can later convert to full accounts.

### Example


```python
import mudbase
from mudbase.models.create_anonymous_session200_response import CreateAnonymousSession200Response
from mudbase.models.create_anonymous_session_request import CreateAnonymousSessionRequest
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
    api_instance = mudbase.AuthenticationApi(api_client)
    create_anonymous_session_request = {"projectId":"685ad30be129932fbb7a1047","deviceId":"device-uuid-123"} # CreateAnonymousSessionRequest |  (optional)

    try:
        # Create anonymous session
        api_response = api_instance.create_anonymous_session(create_anonymous_session_request=create_anonymous_session_request)
        print("The response of AuthenticationApi->create_anonymous_session:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AuthenticationApi->create_anonymous_session: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **create_anonymous_session_request** | [**CreateAnonymousSessionRequest**](CreateAnonymousSessionRequest.md)|  | [optional] 

### Return type

[**CreateAnonymousSession200Response**](CreateAnonymousSession200Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Anonymous session created |  -  |
**400** | Bad request |  -  |
**403** | Access denied |  -  |
**404** | Resource not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_available_o_auth_providers**
> GetAvailableOAuthProviders200Response get_available_o_auth_providers()

Get all available OAuth providers

Returns a list of all supported OAuth providers with their configuration details

### Example


```python
import mudbase
from mudbase.models.get_available_o_auth_providers200_response import GetAvailableOAuthProviders200Response
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
    api_instance = mudbase.AuthenticationApi(api_client)

    try:
        # Get all available OAuth providers
        api_response = api_instance.get_available_o_auth_providers()
        print("The response of AuthenticationApi->get_available_o_auth_providers:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AuthenticationApi->get_available_o_auth_providers: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

[**GetAvailableOAuthProviders200Response**](GetAvailableOAuthProviders200Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | List of available OAuth providers |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_current_session**
> SessionResponse get_current_session()

Get current session

Get the current authenticated user session information.
Requires JWT Bearer token authentication. Both OrgBearerAuth and ProjectBearerAuth are supported (they use the same JWT token format). API keys are not supported for this endpoint.


### Example

* Bearer (JWT) Authentication (OrgBearerAuth):
* Bearer (JWT) Authentication (ProjectBearerAuth):

```python
import mudbase
from mudbase.models.session_response import SessionResponse
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
    api_instance = mudbase.AuthenticationApi(api_client)

    try:
        # Get current session
        api_response = api_instance.get_current_session()
        print("The response of AuthenticationApi->get_current_session:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AuthenticationApi->get_current_session: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

[**SessionResponse**](SessionResponse.md)

### Authorization

[OrgBearerAuth](../README.md#OrgBearerAuth), [ProjectBearerAuth](../README.md#ProjectBearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Current session |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_local_session**
> GetLocalSession200Response get_local_session(project_id=project_id)

Get current session (project-based)

Get the current authenticated user session (project-based).
Requires JWT Bearer token authentication. Both OrgBearerAuth and ProjectBearerAuth are supported (they use the same JWT token format). API keys are not supported for this endpoint.


### Example

* Bearer (JWT) Authentication (OrgBearerAuth):
* Bearer (JWT) Authentication (ProjectBearerAuth):

```python
import mudbase
from mudbase.models.get_local_session200_response import GetLocalSession200Response
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
    api_instance = mudbase.AuthenticationApi(api_client)
    project_id = 'project_id_example' # str |  (optional)

    try:
        # Get current session (project-based)
        api_response = api_instance.get_local_session(project_id=project_id)
        print("The response of AuthenticationApi->get_local_session:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AuthenticationApi->get_local_session: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **str**|  | [optional] 

### Return type

[**GetLocalSession200Response**](GetLocalSession200Response.md)

### Authorization

[OrgBearerAuth](../README.md#OrgBearerAuth), [ProjectBearerAuth](../README.md#ProjectBearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Current session |  -  |
**401** | Authentication required |  -  |
**404** | Resource not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_org_o_auth_providers**
> GetOrgOAuthProviders200Response get_org_o_auth_providers()

Get available OAuth providers for organization-based auth

Returns a list of OAuth providers that are configured and available for organization-based authentication.
Providers are configured via environment variables (e.g., GOOGLE_CLIENT_ID, GITHUB_CLIENT_ID).


### Example


```python
import mudbase
from mudbase.models.get_org_o_auth_providers200_response import GetOrgOAuthProviders200Response
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
    api_instance = mudbase.AuthenticationApi(api_client)

    try:
        # Get available OAuth providers for organization-based auth
        api_response = api_instance.get_org_o_auth_providers()
        print("The response of AuthenticationApi->get_org_o_auth_providers:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AuthenticationApi->get_org_o_auth_providers: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

[**GetOrgOAuthProviders200Response**](GetOrgOAuthProviders200Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | List of available OAuth providers |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **initiate_o_auth**
> initiate_o_auth(provider, project_id, redirect_url=redirect_url)

Initiate OAuth authentication

Initiates OAuth authentication flow for a specified provider and project.
The OAuth provider must be configured and enabled for the project first.
Returns an HTTP 302 redirect to the OAuth provider's consent screen.
Note: Swagger "Try it out" may show "Failed to fetch" for this endpoint due to browser CORS restrictions on cross-origin redirects. Use top-level browser navigation or curl to test.


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
    api_instance = mudbase.AuthenticationApi(api_client)
    provider = 'google' # str | 
    project_id = '685ad30be129932fbb7a1047' # str | 
    redirect_url = 'https://client.app/auth/callback' # str | The URL to redirect to after authentication. Must be pre-registered in project settings. (optional)

    try:
        # Initiate OAuth authentication
        api_instance.initiate_o_auth(provider, project_id, redirect_url=redirect_url)
    except Exception as e:
        print("Exception when calling AuthenticationApi->initiate_o_auth: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **provider** | **str**|  | 
 **project_id** | **str**|  | 
 **redirect_url** | **str**| The URL to redirect to after authentication. Must be pre-registered in project settings. | [optional] 

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
**302** | Redirect to OAuth provider&#39;s consent screen |  * Location - OAuth provider authorization URL <br>  |
**400** | OAuth provider not configured, not enabled, or missing required server/provider credentials |  -  |
**404** | Project not found |  -  |
**500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **initiate_org_o_auth**
> initiate_org_o_auth(provider, redirect_url=redirect_url)

Initiate OAuth authentication for organization

Initiates OAuth authentication flow for organization-level signup/login.
The OAuth provider must be configured via environment variables (e.g., GOOGLE_CLIENT_ID, GOOGLE_CLIENT_SECRET).
After successful authentication, creates a new organization and user account, or logs in existing user.


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
    api_instance = mudbase.AuthenticationApi(api_client)
    provider = 'google' # str | 
    redirect_url = 'https://client.app/auth/callback' # str | The URL to redirect to after authentication (optional)

    try:
        # Initiate OAuth authentication for organization
        api_instance.initiate_org_o_auth(provider, redirect_url=redirect_url)
    except Exception as e:
        print("Exception when calling AuthenticationApi->initiate_org_o_auth: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **provider** | **str**|  | 
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
**302** | Redirect to OAuth provider&#39;s consent screen |  * Location - OAuth provider authorization URL <br>  |
**400** | OAuth provider not configured or not supported |  -  |
**500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **login_local_user**
> LoginLocalUser200Response login_local_user(login_local_user_request)

Login user (project-based)

When the project has **requireEmailVerification** enabled and the user has not verified their email, returns 403 with code **EMAIL_VERIFICATION_REQUIRED** (user must verify email first, then login again).


### Example


```python
import mudbase
from mudbase.models.login_local_user200_response import LoginLocalUser200Response
from mudbase.models.login_local_user_request import LoginLocalUserRequest
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
    api_instance = mudbase.AuthenticationApi(api_client)
    login_local_user_request = {"email":"sarah.chen@example.com","password":"SecurePass123!","projectId":"685ad30be129932fbb7a1047"} # LoginLocalUserRequest | 

    try:
        # Login user (project-based)
        api_response = api_instance.login_local_user(login_local_user_request)
        print("The response of AuthenticationApi->login_local_user:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AuthenticationApi->login_local_user: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **login_local_user_request** | [**LoginLocalUserRequest**](LoginLocalUserRequest.md)|  | 

### Return type

[**LoginLocalUser200Response**](LoginLocalUser200Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Login successful |  -  |
**401** | Authentication required |  -  |
**403** | Email verification required (project has requireEmailVerification and user has not verified) |  -  |
**429** | Rate limit exceeded |  -  |
**500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **login_user**
> AuthResponse login_user(login_request)

Login user

### Example


```python
import mudbase
from mudbase.models.auth_response import AuthResponse
from mudbase.models.login_request import LoginRequest
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
    api_instance = mudbase.AuthenticationApi(api_client)
    login_request = {"email":"john.doe@mudbase.dev","password":"SecurePass123!"} # LoginRequest | 

    try:
        # Login user
        api_response = api_instance.login_user(login_request)
        print("The response of AuthenticationApi->login_user:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AuthenticationApi->login_user: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **login_request** | [**LoginRequest**](LoginRequest.md)|  | 

### Return type

[**AuthResponse**](AuthResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Login successful |  -  |
**401** | Authentication required |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **logout_local_user**
> MessageResponse logout_local_user()

Logout user (project-based)

Logout the current authenticated user session (project-based).
Requires JWT Bearer token authentication. Both OrgBearerAuth and ProjectBearerAuth are supported (they use the same JWT token format). API keys are not supported for this endpoint.


### Example

* Bearer (JWT) Authentication (OrgBearerAuth):
* Bearer (JWT) Authentication (ProjectBearerAuth):

```python
import mudbase
from mudbase.models.message_response import MessageResponse
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
    api_instance = mudbase.AuthenticationApi(api_client)

    try:
        # Logout user (project-based)
        api_response = api_instance.logout_local_user()
        print("The response of AuthenticationApi->logout_local_user:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AuthenticationApi->logout_local_user: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

[**MessageResponse**](MessageResponse.md)

### Authorization

[OrgBearerAuth](../README.md#OrgBearerAuth), [ProjectBearerAuth](../README.md#ProjectBearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Logout successful |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **logout_user**
> MessageResponse logout_user()

Logout user

Logout the current authenticated user session.
Requires JWT Bearer token authentication. Both OrgBearerAuth and ProjectBearerAuth are supported (they use the same JWT token format). API keys are not supported for this endpoint.


### Example

* Bearer (JWT) Authentication (OrgBearerAuth):
* Bearer (JWT) Authentication (ProjectBearerAuth):

```python
import mudbase
from mudbase.models.message_response import MessageResponse
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
    api_instance = mudbase.AuthenticationApi(api_client)

    try:
        # Logout user
        api_response = api_instance.logout_user()
        print("The response of AuthenticationApi->logout_user:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AuthenticationApi->logout_user: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

[**MessageResponse**](MessageResponse.md)

### Authorization

[OrgBearerAuth](../README.md#OrgBearerAuth), [ProjectBearerAuth](../README.md#ProjectBearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Logout successful |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **oauth_callback**
> oauth_callback(provider)

OAuth callback handler (project-based)

Handles OAuth callback for project-based authentication.
This route must be matched before /api/auth/oauth/{provider}/{projectId}.
Redirects to frontend with query params token, refreshToken, and expiresIn.


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
    api_instance = mudbase.AuthenticationApi(api_client)
    provider = 'provider_example' # str | 

    try:
        # OAuth callback handler (project-based)
        api_instance.oauth_callback(provider)
    except Exception as e:
        print("Exception when calling AuthenticationApi->oauth_callback: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **provider** | **str**|  | 

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
**302** | Redirect with token, refreshToken, and expiresIn |  * Location - URL with token, refreshToken, expiresIn query params <br>  |
**400** | Bad request |  -  |
**429** | Rate limit exceeded |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **org_o_auth_callback**
> org_o_auth_callback(provider, code=code, state=state)

OAuth callback handler for organization

Handles OAuth callback for organization-based authentication.
Creates a new organization and user account if the user doesn't exist,
or logs in existing user. Redirects to frontend with query params token, refreshToken, and expiresIn.


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
    api_instance = mudbase.AuthenticationApi(api_client)
    provider = 'google' # str | 
    code = 'code_example' # str | Authorization code from OAuth provider (optional)
    state = 'state_example' # str | State parameter for CSRF protection (optional)

    try:
        # OAuth callback handler for organization
        api_instance.org_o_auth_callback(provider, code=code, state=state)
    except Exception as e:
        print("Exception when calling AuthenticationApi->org_o_auth_callback: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **provider** | **str**|  | 
 **code** | **str**| Authorization code from OAuth provider | [optional] 
 **state** | **str**| State parameter for CSRF protection | [optional] 

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
**302** | Redirect with authentication result |  * Location - OAuth provider authorization URL <br>  |
**400** | OAuth authentication failed |  -  |
**500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **refresh_token**
> RefreshToken200Response refresh_token(refresh_token_request)

Refresh access token (org and project)

Exchange a valid refresh token for a new JWT access token and refresh token.
Works for both **org-based** (platform/dashboard) and **project-based** auth; the same endpoint is used.
The previous refresh token is invalidated (rotation). If the same refresh token is used again, the session is revoked (reuse detection).


### Example


```python
import mudbase
from mudbase.models.refresh_token200_response import RefreshToken200Response
from mudbase.models.refresh_token_request import RefreshTokenRequest
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
    api_instance = mudbase.AuthenticationApi(api_client)
    refresh_token_request = {"refreshToken":"eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9..."} # RefreshTokenRequest | 

    try:
        # Refresh access token (org and project)
        api_response = api_instance.refresh_token(refresh_token_request)
        print("The response of AuthenticationApi->refresh_token:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AuthenticationApi->refresh_token: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **refresh_token_request** | [**RefreshTokenRequest**](RefreshTokenRequest.md)|  | 

### Return type

[**RefreshToken200Response**](RefreshToken200Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | New token pair issued |  -  |
**400** | Missing refresh token |  -  |
**401** | Invalid or expired refresh token (or reuse detected) |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **register_local_user**
> RegisterLocalUser201Response register_local_user(register_local_user_request)

Register new user (project-based)

When the project has **requireEmailVerification** enabled (default), the response is 201 with **requireVerification: true** and **no token**; the user must verify their email then sign in via login. When email verification is disabled, a token and refreshToken are returned.


### Example


```python
import mudbase
from mudbase.models.register_local_user201_response import RegisterLocalUser201Response
from mudbase.models.register_local_user_request import RegisterLocalUserRequest
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
    api_instance = mudbase.AuthenticationApi(api_client)
    register_local_user_request = {"email":"sarah.chen@example.com","password":"SecurePass123!","firstName":"Sarah","lastName":"Chen","projectId":"685ad30be129932fbb7a1047"} # RegisterLocalUserRequest | 

    try:
        # Register new user (project-based)
        api_response = api_instance.register_local_user(register_local_user_request)
        print("The response of AuthenticationApi->register_local_user:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AuthenticationApi->register_local_user: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **register_local_user_request** | [**RegisterLocalUserRequest**](RegisterLocalUserRequest.md)|  | 

### Return type

[**RegisterLocalUser201Response**](RegisterLocalUser201Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | When project.requireEmailVerification is on (default): no token returned; use requireVerification and message to prompt email verification, then user signs in via login. When off: token and refreshToken returned.  |  -  |
**400** | Bad request |  -  |
**404** | Resource not found |  -  |
**429** | Rate limit exceeded |  -  |
**500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **register_user**
> AuthResponse register_user(register_request)

Register new user

### Example


```python
import mudbase
from mudbase.models.auth_response import AuthResponse
from mudbase.models.register_request import RegisterRequest
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
    api_instance = mudbase.AuthenticationApi(api_client)
    register_request = {"email":"john.doe@mudbase.dev","password":"SecurePass123!","firstName":"John","lastName":"Doe","orgName":"Mudbase"} # RegisterRequest | 

    try:
        # Register new user
        api_response = api_instance.register_user(register_request)
        print("The response of AuthenticationApi->register_user:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AuthenticationApi->register_user: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **register_request** | [**RegisterRequest**](RegisterRequest.md)|  | 

### Return type

[**AuthResponse**](AuthResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | User registered successfully |  -  |
**400** | Bad request |  -  |
**409** | Resource conflict |  -  |
**429** | Rate limit exceeded |  -  |
**500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **request_local_password_reset**
> MessageResponse request_local_password_reset(request_local_password_reset_request)

Request password reset (project-based, OTP)

When projectId is provided, sends a 6-digit OTP to the user's email (project-based reset uses OTP, not link).
When projectId is omitted, sends a token link (org/platform local account). Rate limited.


### Example


```python
import mudbase
from mudbase.models.message_response import MessageResponse
from mudbase.models.request_local_password_reset_request import RequestLocalPasswordResetRequest
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
    api_instance = mudbase.AuthenticationApi(api_client)
    request_local_password_reset_request = {"email":"user@example.com","projectId":"685ad30be129932fbb7a1047"} # RequestLocalPasswordResetRequest | 

    try:
        # Request password reset (project-based, OTP)
        api_response = api_instance.request_local_password_reset(request_local_password_reset_request)
        print("The response of AuthenticationApi->request_local_password_reset:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AuthenticationApi->request_local_password_reset: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **request_local_password_reset_request** | [**RequestLocalPasswordResetRequest**](RequestLocalPasswordResetRequest.md)|  | 

### Return type

[**MessageResponse**](MessageResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | OTP or reset email sent (generic message to prevent enumeration) |  -  |
**400** | Bad request |  -  |
**404** | Resource not found |  -  |
**429** | Too many requests (rate limit) |  -  |
**500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **request_password_reset**
> MessageResponse request_password_reset(request_password_reset_request)

Request password reset (organization / platform)

Sends a password reset link to the user's email. Use this for organization (platform) accounts.
For project-based accounts use POST /api/auth/local/password-reset with projectId (sends OTP instead).


### Example


```python
import mudbase
from mudbase.models.message_response import MessageResponse
from mudbase.models.request_password_reset_request import RequestPasswordResetRequest
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
    api_instance = mudbase.AuthenticationApi(api_client)
    request_password_reset_request = {"email":"john.doe@mudbase.dev"} # RequestPasswordResetRequest | 

    try:
        # Request password reset (organization / platform)
        api_response = api_instance.request_password_reset(request_password_reset_request)
        print("The response of AuthenticationApi->request_password_reset:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AuthenticationApi->request_password_reset: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **request_password_reset_request** | [**RequestPasswordResetRequest**](RequestPasswordResetRequest.md)|  | 

### Return type

[**MessageResponse**](MessageResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Password reset email sent (or generic message to prevent enumeration) |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **resend_verification_auth**
> MessageResponse resend_verification_auth(resend_verification_auth_request)

Resend verification email (no auth)

Sends a new verification email to the given email (and optional project).
For unauthenticated users who have not verified yet. Rate limited (e.g. 3 per 15 min per IP).


### Example


```python
import mudbase
from mudbase.models.message_response import MessageResponse
from mudbase.models.resend_verification_auth_request import ResendVerificationAuthRequest
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
    api_instance = mudbase.AuthenticationApi(api_client)
    resend_verification_auth_request = {"email":"user@example.com"} # ResendVerificationAuthRequest | 

    try:
        # Resend verification email (no auth)
        api_response = api_instance.resend_verification_auth(resend_verification_auth_request)
        print("The response of AuthenticationApi->resend_verification_auth:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AuthenticationApi->resend_verification_auth: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **resend_verification_auth_request** | [**ResendVerificationAuthRequest**](ResendVerificationAuthRequest.md)|  | 

### Return type

[**MessageResponse**](MessageResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Verification email sent (or generic message to prevent enumeration) |  -  |
**400** | Email required |  -  |
**429** | Too many requests (rate limit) |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **reset_local_password**
> MessageResponse reset_local_password(token, reset_local_password_request)

Reset password with token (project-based, legacy)

Legacy token-based completion. Prefer OTP flow: use POST .../password-reset/confirm
with the OTP sent to email for project-based resets.


### Example


```python
import mudbase
from mudbase.models.message_response import MessageResponse
from mudbase.models.reset_local_password_request import ResetLocalPasswordRequest
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
    api_instance = mudbase.AuthenticationApi(api_client)
    token = 'token_example' # str | 
    reset_local_password_request = {"password":"NewSecurePass123!","projectId":"685ad30be129932fbb7a1047"} # ResetLocalPasswordRequest | 

    try:
        # Reset password with token (project-based, legacy)
        api_response = api_instance.reset_local_password(token, reset_local_password_request)
        print("The response of AuthenticationApi->reset_local_password:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AuthenticationApi->reset_local_password: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **token** | **str**|  | 
 **reset_local_password_request** | [**ResetLocalPasswordRequest**](ResetLocalPasswordRequest.md)|  | 

### Return type

[**MessageResponse**](MessageResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Password reset successful |  -  |
**400** | Bad request |  -  |
**500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **reset_password**
> MessageResponse reset_password(token, reset_password_request)

Reset password with token (organization / platform)

Set new password using the token from the reset link. Validate the token first with
POST /api/auth/password-reset/validate before showing the form.
If the user's email was not yet verified, it is marked as verified upon successful reset.


### Example


```python
import mudbase
from mudbase.models.message_response import MessageResponse
from mudbase.models.reset_password_request import ResetPasswordRequest
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
    api_instance = mudbase.AuthenticationApi(api_client)
    token = 'token_example' # str | 
    reset_password_request = {"password":"NewSecurePass123!"} # ResetPasswordRequest | 

    try:
        # Reset password with token (organization / platform)
        api_response = api_instance.reset_password(token, reset_password_request)
        print("The response of AuthenticationApi->reset_password:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AuthenticationApi->reset_password: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **token** | **str**|  | 
 **reset_password_request** | [**ResetPasswordRequest**](ResetPasswordRequest.md)|  | 

### Return type

[**MessageResponse**](MessageResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Password reset successful |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **send_magic_link**
> MessageResponse send_magic_link(magic_link_request)

Send magic link

### Example


```python
import mudbase
from mudbase.models.magic_link_request import MagicLinkRequest
from mudbase.models.message_response import MessageResponse
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
    api_instance = mudbase.AuthenticationApi(api_client)
    magic_link_request = {"email":"user@example.com","projectId":"685ad30be129932fbb7a1047","redirectUrl":"https://app.example.com/auth/callback"} # MagicLinkRequest | 

    try:
        # Send magic link
        api_response = api_instance.send_magic_link(magic_link_request)
        print("The response of AuthenticationApi->send_magic_link:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AuthenticationApi->send_magic_link: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **magic_link_request** | [**MagicLinkRequest**](MagicLinkRequest.md)|  | 

### Return type

[**MessageResponse**](MessageResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Magic link sent |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **send_otp**
> MessageResponse send_otp(otp_send_request)

Send OTP code

### Example


```python
import mudbase
from mudbase.models.message_response import MessageResponse
from mudbase.models.otp_send_request import OTPSendRequest
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
    api_instance = mudbase.AuthenticationApi(api_client)
    otp_send_request = {"email":"user@example.com","projectId":"685ad30be129932fbb7a1047","method":"email"} # OTPSendRequest | 

    try:
        # Send OTP code
        api_response = api_instance.send_otp(otp_send_request)
        print("The response of AuthenticationApi->send_otp:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AuthenticationApi->send_otp: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **otp_send_request** | [**OTPSendRequest**](OTPSendRequest.md)|  | 

### Return type

[**MessageResponse**](MessageResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | OTP sent |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **validate_password_reset_token**
> ValidatePasswordResetToken200Response validate_password_reset_token(validate_password_reset_token_request)

Validate password reset token

Call before showing the "set new password" form. Validates that the token from the reset link
is still valid and not expired. Organization (platform) reset only.


### Example


```python
import mudbase
from mudbase.models.validate_password_reset_token200_response import ValidatePasswordResetToken200Response
from mudbase.models.validate_password_reset_token_request import ValidatePasswordResetTokenRequest
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
    api_instance = mudbase.AuthenticationApi(api_client)
    validate_password_reset_token_request = {"token":"abc123..."} # ValidatePasswordResetTokenRequest | 

    try:
        # Validate password reset token
        api_response = api_instance.validate_password_reset_token(validate_password_reset_token_request)
        print("The response of AuthenticationApi->validate_password_reset_token:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AuthenticationApi->validate_password_reset_token: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **validate_password_reset_token_request** | [**ValidatePasswordResetTokenRequest**](ValidatePasswordResetTokenRequest.md)|  | 

### Return type

[**ValidatePasswordResetToken200Response**](ValidatePasswordResetToken200Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Token is valid |  -  |
**400** | Token invalid or expired |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **verify_email_auth**
> MessageResponse verify_email_auth(verify_email_auth_request)

Verify email address (no auth)

Verifies the user's email using the token from the link sent at signup.
Use this for both organization and project signups (unauthenticated).
Same behavior as POST /api/users/verify-email.


### Example


```python
import mudbase
from mudbase.models.message_response import MessageResponse
from mudbase.models.verify_email_auth_request import VerifyEmailAuthRequest
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
    api_instance = mudbase.AuthenticationApi(api_client)
    verify_email_auth_request = {"token":"verification-token-from-email-link"} # VerifyEmailAuthRequest | 

    try:
        # Verify email address (no auth)
        api_response = api_instance.verify_email_auth(verify_email_auth_request)
        print("The response of AuthenticationApi->verify_email_auth:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AuthenticationApi->verify_email_auth: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **verify_email_auth_request** | [**VerifyEmailAuthRequest**](VerifyEmailAuthRequest.md)|  | 

### Return type

[**MessageResponse**](MessageResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Email verified |  -  |
**400** | Invalid or missing token |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **verify_magic_link**
> AuthResponse verify_magic_link(verify_magic_link_request)

Verify magic link

### Example


```python
import mudbase
from mudbase.models.auth_response import AuthResponse
from mudbase.models.verify_magic_link_request import VerifyMagicLinkRequest
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
    api_instance = mudbase.AuthenticationApi(api_client)
    verify_magic_link_request = {"token":"eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJlbWFpbCI6InVzZXJAZXhhbXBsZS5jb20iLCJwcm9qZWN0SWQiOiI2ODVhZDMwYmUxMjk5MzJmYmI3YTEwNDciLCJpYXQiOjE3NTA3ODA4OTgsImV4cCI6MTc1MDc4NDQ5OH0.example"} # VerifyMagicLinkRequest | 

    try:
        # Verify magic link
        api_response = api_instance.verify_magic_link(verify_magic_link_request)
        print("The response of AuthenticationApi->verify_magic_link:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AuthenticationApi->verify_magic_link: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **verify_magic_link_request** | [**VerifyMagicLinkRequest**](VerifyMagicLinkRequest.md)|  | 

### Return type

[**AuthResponse**](AuthResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Magic link verified |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **verify_otp**
> AuthResponse verify_otp(otp_verify_request)

Verify OTP code

### Example


```python
import mudbase
from mudbase.models.auth_response import AuthResponse
from mudbase.models.otp_verify_request import OTPVerifyRequest
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
    api_instance = mudbase.AuthenticationApi(api_client)
    otp_verify_request = {"identifier":"user@example.com","otp":"123456","projectId":"685ad30be129932fbb7a1047"} # OTPVerifyRequest | 

    try:
        # Verify OTP code
        api_response = api_instance.verify_otp(otp_verify_request)
        print("The response of AuthenticationApi->verify_otp:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AuthenticationApi->verify_otp: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **otp_verify_request** | [**OTPVerifyRequest**](OTPVerifyRequest.md)|  | 

### Return type

[**AuthResponse**](AuthResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | OTP verified |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

