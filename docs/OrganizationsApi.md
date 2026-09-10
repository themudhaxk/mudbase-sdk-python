# mudbase.OrganizationsApi

All URIs are relative to *https://cloud.mudbase.dev*

Method | HTTP request | Description
------------- | ------------- | -------------
[**add_org_custom_domain**](OrganizationsApi.md#add_org_custom_domain) | **POST** /api/orgs/{orgId}/projects/{projectId}/domains | Add a custom domain
[**create_organization**](OrganizationsApi.md#create_organization) | **POST** /api/orgs | ~~Create new organization~~ (disabled)
[**delete_org_custom_domain**](OrganizationsApi.md#delete_org_custom_domain) | **DELETE** /api/orgs/{orgId}/projects/{projectId}/domains/{hostname} | Remove a custom domain
[**delete_organization**](OrganizationsApi.md#delete_organization) | **DELETE** /api/orgs/{orgId} | Delete organization
[**delete_sub_organization**](OrganizationsApi.md#delete_sub_organization) | **DELETE** /api/orgs/{orgId}/suborgs/{suborgId} | ~~Delete sub-organization~~ (deprecated)
[**get_org_custom_domain_dns_instructions**](OrganizationsApi.md#get_org_custom_domain_dns_instructions) | **GET** /api/orgs/{orgId}/projects/{projectId}/domains/{hostname}/dns-instructions | Get DNS TXT record instructions for one hostname
[**get_organization**](OrganizationsApi.md#get_organization) | **GET** /api/orgs/{orgId} | Get organization details by ID
[**get_organization_members**](OrganizationsApi.md#get_organization_members) | **GET** /api/orgs/{orgId}/members | Get organization members
[**get_organization_usage**](OrganizationsApi.md#get_organization_usage) | **GET** /api/orgs/{orgId}/usage | Get organization usage and billing
[**get_organization_users**](OrganizationsApi.md#get_organization_users) | **GET** /api/orgs/{orgId}/users | List organization users with metadata
[**get_project_users**](OrganizationsApi.md#get_project_users) | **GET** /api/orgs/{orgId}/projects/{projectId}/users | List project users with metadata
[**get_sub_organizations**](OrganizationsApi.md#get_sub_organizations) | **GET** /api/orgs/{orgId}/suborgs | ~~Get sub-organizations~~ (deprecated)
[**get_user_overview**](OrganizationsApi.md#get_user_overview) | **GET** /api/orgs/{orgId}/users/{userId}/overview | Get user overview and data footprint
[**internal_custom_domain_addon**](OrganizationsApi.md#internal_custom_domain_addon) | **POST** /internal/org/custom-domain-addon | Enable/disable Growth/Scale custom domain add-on (internal)
[**internal_custom_domain_sweep_status**](OrganizationsApi.md#internal_custom_domain_sweep_status) | **GET** /internal/custom-domain/sweep-status | Custom domain background sweep status (internal)
[**internal_domain_dns_recheck_batch**](OrganizationsApi.md#internal_domain_dns_recheck_batch) | **POST** /internal/domain-dns/recheck-batch | Batch DNS re-verification for drift (internal)
[**internal_provision_enterprise**](OrganizationsApi.md#internal_provision_enterprise) | **POST** /internal/provision-enterprise | Provision enterprise dedicated API/DB (internal)
[**invite_sub_organization_member**](OrganizationsApi.md#invite_sub_organization_member) | **POST** /api/orgs/{orgId}/suborgs/{suborgId}/invite | ~~Invite member to sub-organization~~ (deprecated)
[**invite_team_member**](OrganizationsApi.md#invite_team_member) | **POST** /api/orgs/{orgId}/invite | Invite team member to organization
[**list_org_custom_domains**](OrganizationsApi.md#list_org_custom_domains) | **GET** /api/orgs/{orgId}/projects/{projectId}/domains | List custom domains and DNS verification hints
[**list_organizations**](OrganizationsApi.md#list_organizations) | **GET** /api/orgs | Get all organizations for user
[**org_custom_domain_platform_ready**](OrganizationsApi.md#org_custom_domain_platform_ready) | **POST** /api/orgs/{orgId}/projects/{projectId}/domains/{hostname}/platform-ready | Notify platform ops that hosting or edge work is ready (email)
[**org_custom_domain_submit_cname**](OrganizationsApi.md#org_custom_domain_submit_cname) | **POST** /api/orgs/{orgId}/projects/{projectId}/domains/{hostname}/submit-cname | Custom domain step 2 (optional): org confirms routing CNAME was added
[**org_custom_domain_submit_platform_dns_verification_deprecated**](OrganizationsApi.md#org_custom_domain_submit_platform_dns_verification_deprecated) | **POST** /api/orgs/{orgId}/projects/{projectId}/domains/{hostname}/submit-platform-dns-verification | Deprecated — use POST .../verify-platform-dns
[**org_custom_domain_verify_platform_dns**](OrganizationsApi.md#org_custom_domain_verify_platform_dns) | **POST** /api/orgs/{orgId}/projects/{projectId}/domains/{hostname}/verify-platform-dns | Custom domain step 3: verify platform DNS (manual TXT or managed certificate readiness)
[**patch_org_custom_domain**](OrganizationsApi.md#patch_org_custom_domain) | **PATCH** /api/orgs/{orgId}/projects/{projectId}/domains/{hostname} | Update domain status or regenerate verification token
[**remove_sub_organization_member**](OrganizationsApi.md#remove_sub_organization_member) | **DELETE** /api/orgs/{orgId}/suborgs/{suborgId}/members/{userId} | ~~Remove member from sub-organization~~ (deprecated)
[**remove_team_member**](OrganizationsApi.md#remove_team_member) | **DELETE** /api/orgs/{orgId}/members/{userId} | Remove team member from organization
[**set_org_primary_domain**](OrganizationsApi.md#set_org_primary_domain) | **PATCH** /api/orgs/{orgId}/projects/{projectId}/domains/primary | Set primary custom domain
[**update_member_role**](OrganizationsApi.md#update_member_role) | **PATCH** /api/orgs/{orgId}/members/{userId}/role | Update member role
[**update_organization**](OrganizationsApi.md#update_organization) | **PATCH** /api/orgs/{orgId} | Update organization
[**update_organization_plan**](OrganizationsApi.md#update_organization_plan) | **PATCH** /api/orgs/plan/{orgId} | Update organization plan
[**update_sub_organization**](OrganizationsApi.md#update_sub_organization) | **PATCH** /api/orgs/{orgId}/suborgs/{suborgId} | ~~Update sub-organization~~ (deprecated)
[**update_sub_organization_member_role**](OrganizationsApi.md#update_sub_organization_member_role) | **PATCH** /api/orgs/{orgId}/suborgs/{suborgId}/members/{userId}/role | ~~Update sub-organization member role~~ (deprecated)
[**update_user_account_status**](OrganizationsApi.md#update_user_account_status) | **PATCH** /api/orgs/{orgId}/users/{userId}/status | Update user account status (activate or suspend)
[**verify_org_custom_domain_dns**](OrganizationsApi.md#verify_org_custom_domain_dns) | **POST** /api/orgs/{orgId}/projects/{projectId}/domains/{hostname}/verify-dns | Verify domain ownership via DNS TXT


# **add_org_custom_domain**
> OrgAddDomainResponse add_org_custom_domain(org_id, project_id, add_org_domain_request)

Add a custom domain

Creates a pending domain row; the response **`domain`** uses the compact **`OrgDomainEntryOrgConsole`** shape (**`dnsRecords`** includes the Mudbase ownership TXT).
**`dnsRecords`** may include the Mudbase TXT and routing CNAME only until the Mudbase TXT succeeds and the managed certificate is provisioned.
**`flyCertificateStatus`** is typically omitted until certificate provisioning runs after the first successful **`verify-dns`**.


### Example

* Bearer (JWT) Authentication (OrgBearerAuth):

```python
import mudbase
from mudbase.models.add_org_domain_request import AddOrgDomainRequest
from mudbase.models.org_add_domain_response import OrgAddDomainResponse
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
    api_instance = mudbase.OrganizationsApi(api_client)
    org_id = 'org_id_example' # str | 
    project_id = 'project_id_example' # str | 
    add_org_domain_request = {"hostname":"hostname_example"} # AddOrgDomainRequest | 

    try:
        # Add a custom domain
        api_response = api_instance.add_org_custom_domain(org_id, project_id, add_org_domain_request)
        print("The response of OrganizationsApi->add_org_custom_domain:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling OrganizationsApi->add_org_custom_domain: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**|  | 
 **project_id** | **str**|  | 
 **add_org_domain_request** | [**AddOrgDomainRequest**](AddOrgDomainRequest.md)|  | 

### Return type

[**OrgAddDomainResponse**](OrgAddDomainResponse.md)

### Authorization

[OrgBearerAuth](../README.md#OrgBearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | Domain created; includes dnsRecords and human-readable instructions (no extra GET required). |  -  |
**400** | Validation, limit, or hostname_in_use |  -  |
**429** | domain_rate_limited |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **create_organization**
> create_organization(create_organization_request)

~~Create new organization~~ (disabled)

~~Create a new organization.~~
This endpoint is disabled and kept only for backward compatibility in documentation.
Requires: OrgBearerAuth (organization-level authentication only).


### Example

* Bearer (JWT) Authentication (OrgBearerAuth):

```python
import mudbase
from mudbase.models.create_organization_request import CreateOrganizationRequest
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
    api_instance = mudbase.OrganizationsApi(api_client)
    create_organization_request = {"name":"Mudbase Inc","description":"Main organization","logo":"https://example.com/logo.png","website":"https://mudbase.dev","parentOrgId":"685acbe0e129932fbb7a0fc3"} # CreateOrganizationRequest | 

    try:
        # ~~Create new organization~~ (disabled)
        api_instance.create_organization(create_organization_request)
    except Exception as e:
        print("Exception when calling OrganizationsApi->create_organization: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **create_organization_request** | [**CreateOrganizationRequest**](CreateOrganizationRequest.md)|  | 

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
**403** | Organization creation disabled |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_org_custom_domain**
> delete_org_custom_domain(org_id, project_id, hostname)

Remove a custom domain

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
    api_instance = mudbase.OrganizationsApi(api_client)
    org_id = 'org_id_example' # str | 
    project_id = 'project_id_example' # str | 
    hostname = 'hostname_example' # str | 

    try:
        # Remove a custom domain
        api_instance.delete_org_custom_domain(org_id, project_id, hostname)
    except Exception as e:
        print("Exception when calling OrganizationsApi->delete_org_custom_domain: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**|  | 
 **project_id** | **str**|  | 
 **hostname** | **str**|  | 

### Return type

void (empty response body)

### Authorization

[OrgBearerAuth](../README.md#OrgBearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Removed |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_organization**
> DeleteOrganization200Response delete_organization(org_id)

Delete organization

Delete an organization permanently. This is a destructive operation.
Requires JWT Bearer token authentication. Both OrgBearerAuth and ProjectBearerAuth are supported (they use the same JWT token format). These are organization-level operations.


### Example

* Bearer (JWT) Authentication (OrgBearerAuth):
* Bearer (JWT) Authentication (ProjectBearerAuth):

```python
import mudbase
from mudbase.models.delete_organization200_response import DeleteOrganization200Response
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
    api_instance = mudbase.OrganizationsApi(api_client)
    org_id = '685acbe0e129932fbb7a0fc3' # str | 

    try:
        # Delete organization
        api_response = api_instance.delete_organization(org_id)
        print("The response of OrganizationsApi->delete_organization:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling OrganizationsApi->delete_organization: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**|  | 

### Return type

[**DeleteOrganization200Response**](DeleteOrganization200Response.md)

### Authorization

[OrgBearerAuth](../README.md#OrgBearerAuth), [ProjectBearerAuth](../README.md#ProjectBearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Organization deleted |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_sub_organization**
> DeleteSubOrganization200Response delete_sub_organization(org_id, suborg_id)

~~Delete sub-organization~~ (deprecated)

### Example

* Bearer (JWT) Authentication (OrgBearerAuth):
* Bearer (JWT) Authentication (ProjectBearerAuth):

```python
import mudbase
from mudbase.models.delete_sub_organization200_response import DeleteSubOrganization200Response
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
    api_instance = mudbase.OrganizationsApi(api_client)
    org_id = '685acbe0e129932fbb7a0fc3' # str | 
    suborg_id = '685acbe0e129932fbb7a0fc4' # str | 

    try:
        # ~~Delete sub-organization~~ (deprecated)
        api_response = api_instance.delete_sub_organization(org_id, suborg_id)
        print("The response of OrganizationsApi->delete_sub_organization:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling OrganizationsApi->delete_sub_organization: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**|  | 
 **suborg_id** | **str**|  | 

### Return type

[**DeleteSubOrganization200Response**](DeleteSubOrganization200Response.md)

### Authorization

[OrgBearerAuth](../README.md#OrgBearerAuth), [ProjectBearerAuth](../README.md#ProjectBearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Sub-organization deleted |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_org_custom_domain_dns_instructions**
> OrgDnsInstructionsResponse get_org_custom_domain_dns_instructions(org_id, project_id, hostname)

Get DNS TXT record instructions for one hostname

Returns the same shape as list/add for one hostname (URL-encode `hostname` in the path), including **`dnsRecords`** and **`flyCertificateStatus`** when applicable.
See **`listOrgCustomDomains`** for how managed certificate provisioning affects those fields.


### Example

* Bearer (JWT) Authentication (OrgBearerAuth):

```python
import mudbase
from mudbase.models.org_dns_instructions_response import OrgDnsInstructionsResponse
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
    api_instance = mudbase.OrganizationsApi(api_client)
    org_id = 'org_id_example' # str | 
    project_id = 'project_id_example' # str | 
    hostname = 'hostname_example' # str | 

    try:
        # Get DNS TXT record instructions for one hostname
        api_response = api_instance.get_org_custom_domain_dns_instructions(org_id, project_id, hostname)
        print("The response of OrganizationsApi->get_org_custom_domain_dns_instructions:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling OrganizationsApi->get_org_custom_domain_dns_instructions: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**|  | 
 **project_id** | **str**|  | 
 **hostname** | **str**|  | 

### Return type

[**OrgDnsInstructionsResponse**](OrgDnsInstructionsResponse.md)

### Authorization

[OrgBearerAuth](../README.md#OrgBearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Domain row with DNS hints |  -  |
**401** | Unauthorized |  -  |
**403** | Forbidden |  -  |
**404** | domain_not_found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_organization**
> Organization get_organization(org_id)

Get organization details by ID

Get organization details by ID.
Requires: OrgBearerAuth (organization-level authentication only).


### Example

* Bearer (JWT) Authentication (OrgBearerAuth):

```python
import mudbase
from mudbase.models.organization import Organization
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
    api_instance = mudbase.OrganizationsApi(api_client)
    org_id = '685acbe0e129932fbb7a0fc3' # str | 

    try:
        # Get organization details by ID
        api_response = api_instance.get_organization(org_id)
        print("The response of OrganizationsApi->get_organization:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling OrganizationsApi->get_organization: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**|  | 

### Return type

[**Organization**](Organization.md)

### Authorization

[OrgBearerAuth](../README.md#OrgBearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Organization details |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_organization_members**
> GetOrganizationMembers200Response get_organization_members(org_id)

Get organization members

Get all members of an organization. Requires organization-level authentication (JWT Bearer token). API keys are not supported for this endpoint.


### Example

* Bearer (JWT) Authentication (OrgBearerAuth):

```python
import mudbase
from mudbase.models.get_organization_members200_response import GetOrganizationMembers200Response
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
    api_instance = mudbase.OrganizationsApi(api_client)
    org_id = '685acbe0e129932fbb7a0fc3' # str | 

    try:
        # Get organization members
        api_response = api_instance.get_organization_members(org_id)
        print("The response of OrganizationsApi->get_organization_members:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling OrganizationsApi->get_organization_members: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**|  | 

### Return type

[**GetOrganizationMembers200Response**](GetOrganizationMembers200Response.md)

### Authorization

[OrgBearerAuth](../README.md#OrgBearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Organization members |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_organization_usage**
> GetOrganizationUsage200Response get_organization_usage(org_id)

Get organization usage and billing

Get usage statistics and billing information for an organization.
Requires: OrgBearerAuth (organization-level authentication only).


### Example

* Bearer (JWT) Authentication (OrgBearerAuth):

```python
import mudbase
from mudbase.models.get_organization_usage200_response import GetOrganizationUsage200Response
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
    api_instance = mudbase.OrganizationsApi(api_client)
    org_id = '685acbe0e129932fbb7a0fc3' # str | 

    try:
        # Get organization usage and billing
        api_response = api_instance.get_organization_usage(org_id)
        print("The response of OrganizationsApi->get_organization_usage:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling OrganizationsApi->get_organization_usage: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**|  | 

### Return type

[**GetOrganizationUsage200Response**](GetOrganizationUsage200Response.md)

### Authorization

[OrgBearerAuth](../README.md#OrgBearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Usage and billing information |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_organization_users**
> GetOrganizationUsers200Response get_organization_users(org_id, status=status)

List organization users with metadata

Get all users in the organization with metadata (email, full name, role, accountStatus, phone, lastLogin, etc.).
Optional query `status` filters by accountStatus (pending, active, suspended). Requires organization access and owner or admin role.


### Example

* Bearer (JWT) Authentication (OrgBearerAuth):

```python
import mudbase
from mudbase.models.get_organization_users200_response import GetOrganizationUsers200Response
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
    api_instance = mudbase.OrganizationsApi(api_client)
    org_id = '685acbe0e129932fbb7a0fc3' # str | 
    status = 'status_example' # str | Filter by account status (pending, active, suspended) (optional)

    try:
        # List organization users with metadata
        api_response = api_instance.get_organization_users(org_id, status=status)
        print("The response of OrganizationsApi->get_organization_users:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling OrganizationsApi->get_organization_users: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**|  | 
 **status** | **str**| Filter by account status (pending, active, suspended) | [optional] 

### Return type

[**GetOrganizationUsers200Response**](GetOrganizationUsers200Response.md)

### Authorization

[OrgBearerAuth](../README.md#OrgBearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Organization users with metadata |  -  |
**401** | Authentication required |  -  |
**403** | Access denied |  -  |
**404** | Resource not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_project_users**
> GetProjectUsers200Response get_project_users(org_id, project_id, status=status)

List project users with metadata

Get all users in a project with metadata (email, full name, role, accountStatus, etc.).
Optional query `status` filters by accountStatus. Project must belong to the organization. Requires owner or admin role.


### Example

* Bearer (JWT) Authentication (OrgBearerAuth):

```python
import mudbase
from mudbase.models.get_project_users200_response import GetProjectUsers200Response
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
    api_instance = mudbase.OrganizationsApi(api_client)
    org_id = '685acbe0e129932fbb7a0fc3' # str | 
    project_id = '685ad30be129932fbb7a1047' # str | 
    status = 'status_example' # str | Filter by account status (pending, active, suspended) (optional)

    try:
        # List project users with metadata
        api_response = api_instance.get_project_users(org_id, project_id, status=status)
        print("The response of OrganizationsApi->get_project_users:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling OrganizationsApi->get_project_users: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**|  | 
 **project_id** | **str**|  | 
 **status** | **str**| Filter by account status (pending, active, suspended) | [optional] 

### Return type

[**GetProjectUsers200Response**](GetProjectUsers200Response.md)

### Authorization

[OrgBearerAuth](../README.md#OrgBearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Project users with metadata |  -  |
**401** | Authentication required |  -  |
**403** | Access denied |  -  |
**404** | Resource not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_sub_organizations**
> GetSubOrganizations200Response get_sub_organizations(org_id)

~~Get sub-organizations~~ (deprecated)

Get all sub-organizations under a parent organization.
Requires: OrgBearerAuth (organization-level authentication only).


### Example

* Bearer (JWT) Authentication (OrgBearerAuth):

```python
import mudbase
from mudbase.models.get_sub_organizations200_response import GetSubOrganizations200Response
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
    api_instance = mudbase.OrganizationsApi(api_client)
    org_id = '685acbe0e129932fbb7a0fc3' # str | 

    try:
        # ~~Get sub-organizations~~ (deprecated)
        api_response = api_instance.get_sub_organizations(org_id)
        print("The response of OrganizationsApi->get_sub_organizations:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling OrganizationsApi->get_sub_organizations: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**|  | 

### Return type

[**GetSubOrganizations200Response**](GetSubOrganizations200Response.md)

### Authorization

[OrgBearerAuth](../README.md#OrgBearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | List of sub-organizations |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_user_overview**
> GetUserOverview200Response get_user_overview(org_id, user_id)

Get user overview and data footprint

Get a user's profile plus footprint (files count/size, sessions, API keys, collections in project).
Use for dashboard to see everything tied to the user. Requires owner or admin role.


### Example

* Bearer (JWT) Authentication (OrgBearerAuth):

```python
import mudbase
from mudbase.models.get_user_overview200_response import GetUserOverview200Response
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
    api_instance = mudbase.OrganizationsApi(api_client)
    org_id = 'org_id_example' # str | 
    user_id = 'user_id_example' # str | 

    try:
        # Get user overview and data footprint
        api_response = api_instance.get_user_overview(org_id, user_id)
        print("The response of OrganizationsApi->get_user_overview:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling OrganizationsApi->get_user_overview: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**|  | 
 **user_id** | **str**|  | 

### Return type

[**GetUserOverview200Response**](GetUserOverview200Response.md)

### Authorization

[OrgBearerAuth](../README.md#OrgBearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | User and footprint |  -  |
**401** | Authentication required |  -  |
**403** | Access denied |  -  |
**404** | Resource not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **internal_custom_domain_addon**
> internal_custom_domain_addon(internal_custom_domain_addon_request)

Enable/disable Growth/Scale custom domain add-on (internal)

### Example

* Api Key Authentication (InternalApiKey):

```python
import mudbase
from mudbase.models.internal_custom_domain_addon_request import InternalCustomDomainAddonRequest
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

# Configure API key authorization: InternalApiKey
configuration.api_key['InternalApiKey'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['InternalApiKey'] = 'Bearer'

# Enter a context with an instance of the API client
with mudbase.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = mudbase.OrganizationsApi(api_client)
    internal_custom_domain_addon_request = {"orgId":"orgId_example","enabled":true} # InternalCustomDomainAddonRequest | 

    try:
        # Enable/disable Growth/Scale custom domain add-on (internal)
        api_instance.internal_custom_domain_addon(internal_custom_domain_addon_request)
    except Exception as e:
        print("Exception when calling OrganizationsApi->internal_custom_domain_addon: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **internal_custom_domain_addon_request** | [**InternalCustomDomainAddonRequest**](InternalCustomDomainAddonRequest.md)|  | 

### Return type

void (empty response body)

### Authorization

[InternalApiKey](../README.md#InternalApiKey)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Updated |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **internal_custom_domain_sweep_status**
> internal_custom_domain_sweep_status()

Custom domain background sweep status (internal)

Returns the last automated custom-domain sweep (TXT recheck + certificate provisioning retry), job env flags, and deploy troubleshooting hints when the proxy reports the app is not listening on 0.0.0.0:PORT. Requires header `X-Internal-Api-Key` (same as other /internal routes).

### Example

* Api Key Authentication (InternalApiKey):

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

# Configure API key authorization: InternalApiKey
configuration.api_key['InternalApiKey'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['InternalApiKey'] = 'Bearer'

# Enter a context with an instance of the API client
with mudbase.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = mudbase.OrganizationsApi(api_client)

    try:
        # Custom domain background sweep status (internal)
        api_instance.internal_custom_domain_sweep_status()
    except Exception as e:
        print("Exception when calling OrganizationsApi->internal_custom_domain_sweep_status: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

void (empty response body)

### Authorization

[InternalApiKey](../README.md#InternalApiKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | sweep payload, jobConfig, flyHttpListenTroubleshooting |  -  |
**401** | Unauthorized |  -  |
**503** | INTERNAL_API_KEY not configured |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **internal_domain_dns_recheck_batch**
> internal_domain_dns_recheck_batch(internal_domain_dns_recheck_batch_request=internal_domain_dns_recheck_batch_request)

Batch DNS re-verification for drift (internal)

### Example

* Api Key Authentication (InternalApiKey):

```python
import mudbase
from mudbase.models.internal_domain_dns_recheck_batch_request import InternalDomainDnsRecheckBatchRequest
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

# Configure API key authorization: InternalApiKey
configuration.api_key['InternalApiKey'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['InternalApiKey'] = 'Bearer'

# Enter a context with an instance of the API client
with mudbase.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = mudbase.OrganizationsApi(api_client)
    internal_domain_dns_recheck_batch_request = {"maxOrgs":1,"recheckOlderThanHours":1} # InternalDomainDnsRecheckBatchRequest |  (optional)

    try:
        # Batch DNS re-verification for drift (internal)
        api_instance.internal_domain_dns_recheck_batch(internal_domain_dns_recheck_batch_request=internal_domain_dns_recheck_batch_request)
    except Exception as e:
        print("Exception when calling OrganizationsApi->internal_domain_dns_recheck_batch: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **internal_domain_dns_recheck_batch_request** | [**InternalDomainDnsRecheckBatchRequest**](InternalDomainDnsRecheckBatchRequest.md)|  | [optional] 

### Return type

void (empty response body)

### Authorization

[InternalApiKey](../README.md#InternalApiKey)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Summary counts |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **internal_provision_enterprise**
> internal_provision_enterprise(provision_enterprise_request)

Provision enterprise dedicated API/DB (internal)

### Example

* Api Key Authentication (InternalApiKey):

```python
import mudbase
from mudbase.models.provision_enterprise_request import ProvisionEnterpriseRequest
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

# Configure API key authorization: InternalApiKey
configuration.api_key['InternalApiKey'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['InternalApiKey'] = 'Bearer'

# Enter a context with an instance of the API client
with mudbase.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = mudbase.OrganizationsApi(api_client)
    provision_enterprise_request = {"orgId":"orgId_example","provisionRequestId":"provisionRequestId_example","apiBaseUrl":"apiBaseUrl_example","dbRef":"dbRef_example","serverId":"serverId_example"} # ProvisionEnterpriseRequest | 

    try:
        # Provision enterprise dedicated API/DB (internal)
        api_instance.internal_provision_enterprise(provision_enterprise_request)
    except Exception as e:
        print("Exception when calling OrganizationsApi->internal_provision_enterprise: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **provision_enterprise_request** | [**ProvisionEnterpriseRequest**](ProvisionEnterpriseRequest.md)|  | 

### Return type

void (empty response body)

### Authorization

[InternalApiKey](../README.md#InternalApiKey)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Applied or idempotent no-op |  -  |
**403** | not_enterprise_plan |  -  |
**409** | provision_conflict |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **invite_sub_organization_member**
> InviteSubOrganizationMember200Response invite_sub_organization_member(org_id, suborg_id, invite_member_request)

~~Invite member to sub-organization~~ (deprecated)

### Example

* Bearer (JWT) Authentication (OrgBearerAuth):
* Bearer (JWT) Authentication (ProjectBearerAuth):

```python
import mudbase
from mudbase.models.invite_member_request import InviteMemberRequest
from mudbase.models.invite_sub_organization_member200_response import InviteSubOrganizationMember200Response
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
    api_instance = mudbase.OrganizationsApi(api_client)
    org_id = '685acbe0e129932fbb7a0fc3' # str | 
    suborg_id = '685acbe0e129932fbb7a0fc4' # str | 
    invite_member_request = {"email":"user@suborg.example.com","role":"viewer"} # InviteMemberRequest | 

    try:
        # ~~Invite member to sub-organization~~ (deprecated)
        api_response = api_instance.invite_sub_organization_member(org_id, suborg_id, invite_member_request)
        print("The response of OrganizationsApi->invite_sub_organization_member:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling OrganizationsApi->invite_sub_organization_member: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**|  | 
 **suborg_id** | **str**|  | 
 **invite_member_request** | [**InviteMemberRequest**](InviteMemberRequest.md)|  | 

### Return type

[**InviteSubOrganizationMember200Response**](InviteSubOrganizationMember200Response.md)

### Authorization

[OrgBearerAuth](../README.md#OrgBearerAuth), [ProjectBearerAuth](../README.md#ProjectBearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Invitation sent |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **invite_team_member**
> InviteTeamMember200Response invite_team_member(org_id, invite_member_request)

Invite team member to organization

Send an invitation to a user to join the organization.
Requires JWT Bearer token authentication. Both OrgBearerAuth and ProjectBearerAuth are supported (they use the same JWT token format). These are organization-level operations.


### Example

* Bearer (JWT) Authentication (OrgBearerAuth):
* Bearer (JWT) Authentication (ProjectBearerAuth):

```python
import mudbase
from mudbase.models.invite_member_request import InviteMemberRequest
from mudbase.models.invite_team_member200_response import InviteTeamMember200Response
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
    api_instance = mudbase.OrganizationsApi(api_client)
    org_id = '685acbe0e129932fbb7a0fc3' # str | 
    invite_member_request = {"email":"newuser@example.com","role":"member"} # InviteMemberRequest | 

    try:
        # Invite team member to organization
        api_response = api_instance.invite_team_member(org_id, invite_member_request)
        print("The response of OrganizationsApi->invite_team_member:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling OrganizationsApi->invite_team_member: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**|  | 
 **invite_member_request** | [**InviteMemberRequest**](InviteMemberRequest.md)|  | 

### Return type

[**InviteTeamMember200Response**](InviteTeamMember200Response.md)

### Authorization

[OrgBearerAuth](../README.md#OrgBearerAuth), [ProjectBearerAuth](../README.md#ProjectBearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Invitation sent |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_org_custom_domains**
> OrgDomainsListResponse list_org_custom_domains(org_id, project_id)

List custom domains and DNS verification hints

Returns allowed hostnames for **this project**, primary hostname (per project), API base URL, and per-domain DNS guidance.

Each row uses **`dnsRecords`** for the Mudbase ownership TXT (purpose **`mudbase_ownership`**) and the routing **CNAME** target that Mudbase provisions for the hostname (else the platform default target). Once the ownership TXT has passed at least once, Mudbase provisions and manages the TLS certificate for the hostname automatically and may add further checklist rows (for example `acme_challenge`) needed to complete certificate issuance.
The certificate status field mirrors the managed certificate’s state during issuance (e.g. `pending_validation`, `active`).

Managed edge TLS details are present only on deployments that serve managed edge certificates.

Requires Growth, Scale, or Enterprise plan (custom domains included in plan features).


### Example

* Bearer (JWT) Authentication (OrgBearerAuth):

```python
import mudbase
from mudbase.models.org_domains_list_response import OrgDomainsListResponse
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
    api_instance = mudbase.OrganizationsApi(api_client)
    org_id = 'org_id_example' # str | 
    project_id = 'project_id_example' # str | 

    try:
        # List custom domains and DNS verification hints
        api_response = api_instance.list_org_custom_domains(org_id, project_id)
        print("The response of OrganizationsApi->list_org_custom_domains:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling OrganizationsApi->list_org_custom_domains: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**|  | 
 **project_id** | **str**|  | 

### Return type

[**OrgDomainsListResponse**](OrgDomainsListResponse.md)

### Authorization

[OrgBearerAuth](../README.md#OrgBearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Domain list and hints |  -  |
**401** | Unauthorized |  -  |
**403** | Forbidden |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_organizations**
> ListOrganizations200Response list_organizations()

Get all organizations for user

Get all organizations the authenticated user belongs to.
Requires: OrgBearerAuth (organization-level authentication only).


### Example

* Bearer (JWT) Authentication (OrgBearerAuth):

```python
import mudbase
from mudbase.models.list_organizations200_response import ListOrganizations200Response
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
    api_instance = mudbase.OrganizationsApi(api_client)

    try:
        # Get all organizations for user
        api_response = api_instance.list_organizations()
        print("The response of OrganizationsApi->list_organizations:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling OrganizationsApi->list_organizations: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

[**ListOrganizations200Response**](ListOrganizations200Response.md)

### Authorization

[OrgBearerAuth](../README.md#OrgBearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | List of organizations |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **org_custom_domain_platform_ready**
> org_custom_domain_platform_ready(org_id, project_id, hostname, org_custom_domain_platform_ready_request=org_custom_domain_platform_ready_request)

Notify platform ops that hosting or edge work is ready (email)

Legacy optional ping: ops are emailed automatically on first successful Mudbase TXT verify. Use this only for an extra nudge.
Sends an email to ops while the domain is in platform setup (after Mudbase TXT verification through later pipeline states).
Recipients default to `admin@mudhaxkservices.com` and `admin@mudbase.dev` when `CUSTOM_DOMAIN_OPS_NOTIFY_EMAILS` is unset; override with that env (comma/space-separated).
Returns **503** `email_provider_not_configured` if the platform email provider is not configured.


### Example

* Bearer (JWT) Authentication (OrgBearerAuth):

```python
import mudbase
from mudbase.models.org_custom_domain_platform_ready_request import OrgCustomDomainPlatformReadyRequest
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
    api_instance = mudbase.OrganizationsApi(api_client)
    org_id = 'org_id_example' # str | 
    project_id = 'project_id_example' # str | 
    hostname = 'hostname_example' # str | 
    org_custom_domain_platform_ready_request = {"note":"note_example"} # OrgCustomDomainPlatformReadyRequest |  (optional)

    try:
        # Notify platform ops that hosting or edge work is ready (email)
        api_instance.org_custom_domain_platform_ready(org_id, project_id, hostname, org_custom_domain_platform_ready_request=org_custom_domain_platform_ready_request)
    except Exception as e:
        print("Exception when calling OrganizationsApi->org_custom_domain_platform_ready: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**|  | 
 **project_id** | **str**|  | 
 **hostname** | **str**|  | 
 **org_custom_domain_platform_ready_request** | [**OrgCustomDomainPlatformReadyRequest**](OrgCustomDomainPlatformReadyRequest.md)|  | [optional] 

### Return type

void (empty response body)

### Authorization

[OrgBearerAuth](../README.md#OrgBearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Ops notified |  -  |
**400** | custom_domain_invalid_state |  -  |
**401** | Unauthorized |  -  |
**403** | Forbidden |  -  |
**503** | email_provider_not_configured — email provider not configured on the server |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **org_custom_domain_submit_cname**
> OrgPatchDomainResponse org_custom_domain_submit_cname(org_id, project_id, hostname)

Custom domain step 2 (optional): org confirms routing CNAME was added

Usually unnecessary. With automated certificate provisioning, the Mudbase TXT verify may already set `cname_approved`. Legacy pipelines may queue `cname_pending_staff` until staff **`approve-cname`**.
Use **`routingCnameTarget`** from **`GET .../projects/{projectId}/domains`** (the managed routing CNAME target when provisioned, else the platform default target).


### Example

* Bearer (JWT) Authentication (OrgBearerAuth):

```python
import mudbase
from mudbase.models.org_patch_domain_response import OrgPatchDomainResponse
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
    api_instance = mudbase.OrganizationsApi(api_client)
    org_id = 'org_id_example' # str | 
    project_id = 'project_id_example' # str | 
    hostname = 'hostname_example' # str | 

    try:
        # Custom domain step 2 (optional): org confirms routing CNAME was added
        api_response = api_instance.org_custom_domain_submit_cname(org_id, project_id, hostname)
        print("The response of OrganizationsApi->org_custom_domain_submit_cname:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling OrganizationsApi->org_custom_domain_submit_cname: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**|  | 
 **project_id** | **str**|  | 
 **hostname** | **str**|  | 

### Return type

[**OrgPatchDomainResponse**](OrgPatchDomainResponse.md)

### Authorization

[OrgBearerAuth](../README.md#OrgBearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Updated domain row |  -  |
**400** | custom_domain_invalid_state |  -  |
**401** | Unauthorized |  -  |
**403** | Forbidden |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **org_custom_domain_submit_platform_dns_verification_deprecated**
> OrgPatchDomainResponse org_custom_domain_submit_platform_dns_verification_deprecated(org_id, project_id, hostname)

Deprecated — use POST .../verify-platform-dns

Deprecated alias of **`orgCustomDomainVerifyPlatformDns`** (same behavior: manual TXT and/or automated certificate provisioning per deployment).

### Example

* Bearer (JWT) Authentication (OrgBearerAuth):

```python
import mudbase
from mudbase.models.org_patch_domain_response import OrgPatchDomainResponse
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
    api_instance = mudbase.OrganizationsApi(api_client)
    org_id = 'org_id_example' # str | 
    project_id = 'project_id_example' # str | 
    hostname = 'hostname_example' # str | 

    try:
        # Deprecated — use POST .../verify-platform-dns
        api_response = api_instance.org_custom_domain_submit_platform_dns_verification_deprecated(org_id, project_id, hostname)
        print("The response of OrganizationsApi->org_custom_domain_submit_platform_dns_verification_deprecated:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling OrganizationsApi->org_custom_domain_submit_platform_dns_verification_deprecated: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**|  | 
 **project_id** | **str**|  | 
 **hostname** | **str**|  | 

### Return type

[**OrgPatchDomainResponse**](OrgPatchDomainResponse.md)

### Authorization

[OrgBearerAuth](../README.md#OrgBearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Same as verify-platform-dns |  -  |
**400** | Error |  -  |
**503** | dns_lookup_error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **org_custom_domain_verify_platform_dns**
> OrgPatchDomainResponse org_custom_domain_verify_platform_dns(org_id, project_id, hostname)

Custom domain step 3: verify platform DNS (manual TXT or managed certificate readiness)

**Manual path:** After staff **`PATCH .../platform-dns-verification`**, the org adds the published TXT and calls this endpoint. The API resolves public TXT at **`platformDnsVerification.recordName`** and matches **`recordValue`**. On success, `status` → **`platform_dns_pending_review`** until staff **`POST .../activate`**.

**Automated path (default):** When automated certificate provisioning is in effect, the org calls this after the Mudbase TXT and the certificate DNS rows are in place (status typically **`cname_approved`** from automated verify-dns). The API checks the managed certificate with bounded retries. On success, `status` → **`active`** and the org may receive the activation email, with no staff **`approve-cname`** or **`activate`** required.

**Legacy path:** In the legacy staff pipeline, staff **`approve-cname`** may be required first; after the managed certificate is ready, **`status`** becomes **`active`** on auto-activation, else **`platform_dns_pending_review`** until staff **`activate`**.

**`platform_dns_verification_failed`** may include **`details.flyStatus`** / **`details.flyError`** with provisioning error context.


### Example

* Bearer (JWT) Authentication (OrgBearerAuth):

```python
import mudbase
from mudbase.models.org_patch_domain_response import OrgPatchDomainResponse
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
    api_instance = mudbase.OrganizationsApi(api_client)
    org_id = 'org_id_example' # str | 
    project_id = 'project_id_example' # str | 
    hostname = 'hostname_example' # str | 

    try:
        # Custom domain step 3: verify platform DNS (manual TXT or managed certificate readiness)
        api_response = api_instance.org_custom_domain_verify_platform_dns(org_id, project_id, hostname)
        print("The response of OrganizationsApi->org_custom_domain_verify_platform_dns:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling OrganizationsApi->org_custom_domain_verify_platform_dns: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**|  | 
 **project_id** | **str**|  | 
 **hostname** | **str**|  | 

### Return type

[**OrgPatchDomainResponse**](OrgPatchDomainResponse.md)

### Authorization

[OrgBearerAuth](../README.md#OrgBearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Domain row updated (&#x60;OrgPatchDomainResponse.domain&#x60;). Manual TXT path typically sets &#x60;platform_dns_pending_review&#x60;. Automated provisioning: typically &#x60;active&#x60; when the certificate is ready. Legacy staff pipeline: may set &#x60;platform_dns_pending_review&#x60; unless auto-activation is enabled. Body may include refreshed &#x60;dnsRecords&#x60; and &#x60;flyCertificateStatus&#x60; when certificate provisioning ran. |  -  |
**400** | custom_domain_invalid_state, platform_dns_verification_failed (manual TXT mismatch or managed certificate not active yet; see response details) |  -  |
**401** | Unauthorized |  -  |
**403** | Forbidden |  -  |
**503** | dns_lookup_error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **patch_org_custom_domain**
> OrgPatchDomainResponse patch_org_custom_domain(org_id, project_id, hostname, patch_org_domain_request=patch_org_domain_request)

Update domain status or regenerate verification token

### Example

* Bearer (JWT) Authentication (OrgBearerAuth):

```python
import mudbase
from mudbase.models.org_patch_domain_response import OrgPatchDomainResponse
from mudbase.models.patch_org_domain_request import PatchOrgDomainRequest
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
    api_instance = mudbase.OrganizationsApi(api_client)
    org_id = 'org_id_example' # str | 
    project_id = 'project_id_example' # str | 
    hostname = 'hostname_example' # str | 
    patch_org_domain_request = {"status":"pending","regenerateToken":true} # PatchOrgDomainRequest |  (optional)

    try:
        # Update domain status or regenerate verification token
        api_response = api_instance.patch_org_custom_domain(org_id, project_id, hostname, patch_org_domain_request=patch_org_domain_request)
        print("The response of OrganizationsApi->patch_org_custom_domain:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling OrganizationsApi->patch_org_custom_domain: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**|  | 
 **project_id** | **str**|  | 
 **hostname** | **str**|  | 
 **patch_org_domain_request** | [**PatchOrgDomainRequest**](PatchOrgDomainRequest.md)|  | [optional] 

### Return type

[**OrgPatchDomainResponse**](OrgPatchDomainResponse.md)

### Authorization

[OrgBearerAuth](../README.md#OrgBearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Updated; domain object includes dnsTxtHost and dnsTxtValue |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **remove_sub_organization_member**
> RemoveTeamMember200Response remove_sub_organization_member(org_id, suborg_id, user_id)

~~Remove member from sub-organization~~ (deprecated)

### Example

* Bearer (JWT) Authentication (OrgBearerAuth):
* Bearer (JWT) Authentication (ProjectBearerAuth):

```python
import mudbase
from mudbase.models.remove_team_member200_response import RemoveTeamMember200Response
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
    api_instance = mudbase.OrganizationsApi(api_client)
    org_id = '685acbe0e129932fbb7a0fc3' # str | 
    suborg_id = '685acbe0e129932fbb7a0fc4' # str | 
    user_id = '685acbe0e129932fbb7a0fc2' # str | 

    try:
        # ~~Remove member from sub-organization~~ (deprecated)
        api_response = api_instance.remove_sub_organization_member(org_id, suborg_id, user_id)
        print("The response of OrganizationsApi->remove_sub_organization_member:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling OrganizationsApi->remove_sub_organization_member: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**|  | 
 **suborg_id** | **str**|  | 
 **user_id** | **str**|  | 

### Return type

[**RemoveTeamMember200Response**](RemoveTeamMember200Response.md)

### Authorization

[OrgBearerAuth](../README.md#OrgBearerAuth), [ProjectBearerAuth](../README.md#ProjectBearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Member removed |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **remove_team_member**
> RemoveTeamMember200Response remove_team_member(org_id, user_id)

Remove team member from organization

Remove a user from the organization.
Requires JWT Bearer token authentication. Both OrgBearerAuth and ProjectBearerAuth are supported (they use the same JWT token format). These are organization-level operations.


### Example

* Bearer (JWT) Authentication (OrgBearerAuth):
* Bearer (JWT) Authentication (ProjectBearerAuth):

```python
import mudbase
from mudbase.models.remove_team_member200_response import RemoveTeamMember200Response
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
    api_instance = mudbase.OrganizationsApi(api_client)
    org_id = '685acbe0e129932fbb7a0fc3' # str | 
    user_id = '685acbe0e129932fbb7a0fc2' # str | 

    try:
        # Remove team member from organization
        api_response = api_instance.remove_team_member(org_id, user_id)
        print("The response of OrganizationsApi->remove_team_member:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling OrganizationsApi->remove_team_member: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**|  | 
 **user_id** | **str**|  | 

### Return type

[**RemoveTeamMember200Response**](RemoveTeamMember200Response.md)

### Authorization

[OrgBearerAuth](../README.md#OrgBearerAuth), [ProjectBearerAuth](../README.md#ProjectBearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Member removed |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **set_org_primary_domain**
> set_org_primary_domain(org_id, project_id, set_org_primary_domain_request)

Set primary custom domain

### Example

* Bearer (JWT) Authentication (OrgBearerAuth):

```python
import mudbase
from mudbase.models.set_org_primary_domain_request import SetOrgPrimaryDomainRequest
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
    api_instance = mudbase.OrganizationsApi(api_client)
    org_id = 'org_id_example' # str | 
    project_id = 'project_id_example' # str | 
    set_org_primary_domain_request = {"hostname":"hostname_example"} # SetOrgPrimaryDomainRequest | 

    try:
        # Set primary custom domain
        api_instance.set_org_primary_domain(org_id, project_id, set_org_primary_domain_request)
    except Exception as e:
        print("Exception when calling OrganizationsApi->set_org_primary_domain: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**|  | 
 **project_id** | **str**|  | 
 **set_org_primary_domain_request** | [**SetOrgPrimaryDomainRequest**](SetOrgPrimaryDomainRequest.md)|  | 

### Return type

void (empty response body)

### Authorization

[OrgBearerAuth](../README.md#OrgBearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Primary updated |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_member_role**
> UpdateMemberRole200Response update_member_role(org_id, user_id, update_member_role_request)

Update member role

Update a member's role in the organization. Requires organization-level authentication (JWT Bearer token). API keys are not supported for this endpoint.


### Example

* Bearer (JWT) Authentication (OrgBearerAuth):

```python
import mudbase
from mudbase.models.update_member_role200_response import UpdateMemberRole200Response
from mudbase.models.update_member_role_request import UpdateMemberRoleRequest
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
    api_instance = mudbase.OrganizationsApi(api_client)
    org_id = '685acbe0e129932fbb7a0fc3' # str | 
    user_id = '685acbe0e129932fbb7a0fc2' # str | 
    update_member_role_request = {"role":"admin"} # UpdateMemberRoleRequest | 

    try:
        # Update member role
        api_response = api_instance.update_member_role(org_id, user_id, update_member_role_request)
        print("The response of OrganizationsApi->update_member_role:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling OrganizationsApi->update_member_role: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**|  | 
 **user_id** | **str**|  | 
 **update_member_role_request** | [**UpdateMemberRoleRequest**](UpdateMemberRoleRequest.md)|  | 

### Return type

[**UpdateMemberRole200Response**](UpdateMemberRole200Response.md)

### Authorization

[OrgBearerAuth](../README.md#OrgBearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Role updated |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_organization**
> UpdateOrganization200Response update_organization(org_id, update_organization_request)

Update organization

Update organization details. Requires organization-level authentication (JWT Bearer token). API keys are not supported for this endpoint.


### Example

* Bearer (JWT) Authentication (OrgBearerAuth):

```python
import mudbase
from mudbase.models.update_organization200_response import UpdateOrganization200Response
from mudbase.models.update_organization_request import UpdateOrganizationRequest
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
    api_instance = mudbase.OrganizationsApi(api_client)
    org_id = '685acbe0e129932fbb7a0fc3' # str | 
    update_organization_request = {"name":"Mudbase Inc Updated","description":"Updated organization description","logo":"https://example.com/new-logo.png","website":"https://mudbase.dev"} # UpdateOrganizationRequest | 

    try:
        # Update organization
        api_response = api_instance.update_organization(org_id, update_organization_request)
        print("The response of OrganizationsApi->update_organization:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling OrganizationsApi->update_organization: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**|  | 
 **update_organization_request** | [**UpdateOrganizationRequest**](UpdateOrganizationRequest.md)|  | 

### Return type

[**UpdateOrganization200Response**](UpdateOrganization200Response.md)

### Authorization

[OrgBearerAuth](../README.md#OrgBearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Organization updated |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_organization_plan**
> UpdateOrganizationPlan200Response update_organization_plan(org_id, update_organization_plan_request)

Update organization plan

### Example

* Bearer (JWT) Authentication (OrgBearerAuth):
* Bearer (JWT) Authentication (ProjectBearerAuth):

```python
import mudbase
from mudbase.models.update_organization_plan200_response import UpdateOrganizationPlan200Response
from mudbase.models.update_organization_plan_request import UpdateOrganizationPlanRequest
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
    api_instance = mudbase.OrganizationsApi(api_client)
    org_id = '685acbe0e129932fbb7a0fc3' # str | 
    update_organization_plan_request = {"plan":"pro"} # UpdateOrganizationPlanRequest | 

    try:
        # Update organization plan
        api_response = api_instance.update_organization_plan(org_id, update_organization_plan_request)
        print("The response of OrganizationsApi->update_organization_plan:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling OrganizationsApi->update_organization_plan: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**|  | 
 **update_organization_plan_request** | [**UpdateOrganizationPlanRequest**](UpdateOrganizationPlanRequest.md)|  | 

### Return type

[**UpdateOrganizationPlan200Response**](UpdateOrganizationPlan200Response.md)

### Authorization

[OrgBearerAuth](../README.md#OrgBearerAuth), [ProjectBearerAuth](../README.md#ProjectBearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Plan updated (or error if trying to upgrade to paid) |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_sub_organization**
> UpdateSubOrganization200Response update_sub_organization(org_id, suborg_id, update_organization_request)

~~Update sub-organization~~ (deprecated)

Update a sub-organization's configuration.
Requires JWT Bearer token authentication. Both OrgBearerAuth and ProjectBearerAuth are supported (they use the same JWT token format). These are organization-level operations.


### Example

* Bearer (JWT) Authentication (OrgBearerAuth):
* Bearer (JWT) Authentication (ProjectBearerAuth):

```python
import mudbase
from mudbase.models.update_organization_request import UpdateOrganizationRequest
from mudbase.models.update_sub_organization200_response import UpdateSubOrganization200Response
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
    api_instance = mudbase.OrganizationsApi(api_client)
    org_id = '685acbe0e129932fbb7a0fc3' # str | 
    suborg_id = '685acbe0e129932fbb7a0fc4' # str | 
    update_organization_request = {"name":"Sub-Organization Updated","description":"Updated sub-organization description","logo":"https://example.com/sub-logo.png","website":"https://sub.mudbase.dev"} # UpdateOrganizationRequest | 

    try:
        # ~~Update sub-organization~~ (deprecated)
        api_response = api_instance.update_sub_organization(org_id, suborg_id, update_organization_request)
        print("The response of OrganizationsApi->update_sub_organization:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling OrganizationsApi->update_sub_organization: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**|  | 
 **suborg_id** | **str**|  | 
 **update_organization_request** | [**UpdateOrganizationRequest**](UpdateOrganizationRequest.md)|  | 

### Return type

[**UpdateSubOrganization200Response**](UpdateSubOrganization200Response.md)

### Authorization

[OrgBearerAuth](../README.md#OrgBearerAuth), [ProjectBearerAuth](../README.md#ProjectBearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Sub-organization updated |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_sub_organization_member_role**
> UpdateMemberRole200Response update_sub_organization_member_role(org_id, suborg_id, user_id, update_member_role_request)

~~Update sub-organization member role~~ (deprecated)

### Example

* Bearer (JWT) Authentication (OrgBearerAuth):
* Bearer (JWT) Authentication (ProjectBearerAuth):

```python
import mudbase
from mudbase.models.update_member_role200_response import UpdateMemberRole200Response
from mudbase.models.update_member_role_request import UpdateMemberRoleRequest
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
    api_instance = mudbase.OrganizationsApi(api_client)
    org_id = '685acbe0e129932fbb7a0fc3' # str | 
    suborg_id = '685acbe0e129932fbb7a0fc4' # str | 
    user_id = '685acbe0e129932fbb7a0fc2' # str | 
    update_member_role_request = {"role":"admin"} # UpdateMemberRoleRequest | 

    try:
        # ~~Update sub-organization member role~~ (deprecated)
        api_response = api_instance.update_sub_organization_member_role(org_id, suborg_id, user_id, update_member_role_request)
        print("The response of OrganizationsApi->update_sub_organization_member_role:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling OrganizationsApi->update_sub_organization_member_role: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**|  | 
 **suborg_id** | **str**|  | 
 **user_id** | **str**|  | 
 **update_member_role_request** | [**UpdateMemberRoleRequest**](UpdateMemberRoleRequest.md)|  | 

### Return type

[**UpdateMemberRole200Response**](UpdateMemberRole200Response.md)

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

# **update_user_account_status**
> UpdateUserAccountStatus200Response update_user_account_status(org_id, user_id, update_user_account_status_request)

Update user account status (activate or suspend)

Set a user's account status to active or suspended. Used to approve pending users or suspend/activate accounts.
Cannot change status of an organization owner. Requires owner or admin role.


### Example

* Bearer (JWT) Authentication (OrgBearerAuth):

```python
import mudbase
from mudbase.models.update_user_account_status200_response import UpdateUserAccountStatus200Response
from mudbase.models.update_user_account_status_request import UpdateUserAccountStatusRequest
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
    api_instance = mudbase.OrganizationsApi(api_client)
    org_id = 'org_id_example' # str | 
    user_id = 'user_id_example' # str | 
    update_user_account_status_request = {"accountStatus":"active"} # UpdateUserAccountStatusRequest | 

    try:
        # Update user account status (activate or suspend)
        api_response = api_instance.update_user_account_status(org_id, user_id, update_user_account_status_request)
        print("The response of OrganizationsApi->update_user_account_status:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling OrganizationsApi->update_user_account_status: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**|  | 
 **user_id** | **str**|  | 
 **update_user_account_status_request** | [**UpdateUserAccountStatusRequest**](UpdateUserAccountStatusRequest.md)|  | 

### Return type

[**UpdateUserAccountStatus200Response**](UpdateUserAccountStatus200Response.md)

### Authorization

[OrgBearerAuth](../README.md#OrgBearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | User status updated |  -  |
**400** | Bad request |  -  |
**401** | Authentication required |  -  |
**403** | Access denied |  -  |
**404** | Resource not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **verify_org_custom_domain_dns**
> OrgVerifyCustomDomainDnsSuccessResponse verify_org_custom_domain_dns(org_id, project_id, hostname)

Verify domain ownership via DNS TXT

Looks up TXT at `_mudbase-verify.<hostname>` for value `mudbase-domain-verification=<token>`.

On a successful verify, Mudbase begins provisioning and managing the TLS certificate for the hostname automatically. Depending on the deployment, the response may include managed edge TLS details with domain-control validation (DCV) hints for the certificate.

When automated certificate provisioning is in effect, a successful verify records the certificate’s DNS requirements and status may advance to **`cname_approved`** in the same response (no staff **`approve-cname`** step). Otherwise, first success from `pending`/`failed` may move to **`cname_pending_staff`** and queue platform review as before.

The **200** response may include **`dnsRecords`**, certificate status, and **`routingCnameTarget`** for the managed certificate once its requirements are provisioned.


### Example

* Bearer (JWT) Authentication (OrgBearerAuth):

```python
import mudbase
from mudbase.models.org_verify_custom_domain_dns_success_response import OrgVerifyCustomDomainDnsSuccessResponse
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
    api_instance = mudbase.OrganizationsApi(api_client)
    org_id = 'org_id_example' # str | 
    project_id = 'project_id_example' # str | 
    hostname = 'hostname_example' # str | 

    try:
        # Verify domain ownership via DNS TXT
        api_response = api_instance.verify_org_custom_domain_dns(org_id, project_id, hostname)
        print("The response of OrganizationsApi->verify_org_custom_domain_dns:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling OrganizationsApi->verify_org_custom_domain_dns: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**|  | 
 **project_id** | **str**|  | 
 **hostname** | **str**|  | 

### Return type

[**OrgVerifyCustomDomainDnsSuccessResponse**](OrgVerifyCustomDomainDnsSuccessResponse.md)

### Authorization

[OrgBearerAuth](../README.md#OrgBearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | TXT verified. With automated certificate provisioning, often &#x60;cname_approved&#x60; once DNS requirements are returned; otherwise may show &#x60;cname_pending_staff&#x60; or &#x60;dns_verified&#x60;. Includes &#x60;dnsTxtHost&#x60;/&#x60;dnsTxtValue&#x60;, optional managed edge TLS details, optional &#x60;dnsRecords&#x60; + certificate status when provisioning ran after this verify. |  -  |
**400** | dns_verification_failed (TXT missing or wrong); body includes dnsTxtHost, dnsTxtValue, challengeHost, expectedTxt |  -  |
**503** | dns_lookup_error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

