# mudbase.ComplianceApi

All URIs are relative to *https://cloud.mudbase.dev*

Method | HTTP request | Description
------------- | ------------- | -------------
[**api_gdpr_erase_post**](ComplianceApi.md#api_gdpr_erase_post) | **POST** /api/gdpr/erase | Erase my personal data (GDPR Art. 17)
[**api_gdpr_export_get**](ComplianceApi.md#api_gdpr_export_get) | **GET** /api/gdpr/export | Export my personal data (GDPR Art. 15)
[**generate_access_review**](ComplianceApi.md#generate_access_review) | **POST** /api/compliance/access-review | Generate access review report (SOC 2)
[**generate_data_processing_record**](ComplianceApi.md#generate_data_processing_record) | **POST** /api/compliance/data-processing-record | Generate data processing record (GDPR Article 30)
[**get_compliance_summary**](ComplianceApi.md#get_compliance_summary) | **GET** /api/compliance/summary | Get compliance summary
[**log_security_event**](ComplianceApi.md#log_security_event) | **POST** /api/compliance/security-event | Log security event


# **api_gdpr_erase_post**
> ApplyRoleFeaturePreset200Response api_gdpr_erase_post(api_gdpr_erase_post_request)

Erase my personal data (GDPR Art. 17)

Anonymizes the subject's PII, revokes sessions/tokens, and anonymizes (never hard-deletes)
financial/legal-retention records. Idempotent and self-scoped.

Requires re-proving your current password (skipped only for OAuth-only accounts with no
password set) and, if 2FA is enabled, a fresh TOTP code - the same step-up re-authentication
already required by the less-destructive `PATCH /api/users/password` and
`POST /api/users/2fa/disable`.


### Example

* Bearer (JWT) Authentication (OrgBearerAuth):

```python
import mudbase
from mudbase.models.api_gdpr_erase_post_request import ApiGdprErasePostRequest
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

# Enter a context with an instance of the API client
with mudbase.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = mudbase.ComplianceApi(api_client)
    api_gdpr_erase_post_request = mudbase.ApiGdprErasePostRequest() # ApiGdprErasePostRequest | 

    try:
        # Erase my personal data (GDPR Art. 17)
        api_response = api_instance.api_gdpr_erase_post(api_gdpr_erase_post_request)
        print("The response of ComplianceApi->api_gdpr_erase_post:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ComplianceApi->api_gdpr_erase_post: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **api_gdpr_erase_post_request** | [**ApiGdprErasePostRequest**](ApiGdprErasePostRequest.md)|  | 

### Return type

[**ApplyRoleFeaturePreset200Response**](ApplyRoleFeaturePreset200Response.md)

### Authorization

[OrgBearerAuth](../README.md#OrgBearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Data anonymized (or already anonymized — idempotent) |  -  |
**400** | Confirmation field missing/not equal to \&quot;DELETE\&quot;, or currentPassword/totpToken missing or invalid |  -  |
**401** | Authentication required |  -  |
**409** | Sole owner of one or more organizations - transfer or delete them first |  -  |
**429** | Rate limit exceeded |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **api_gdpr_export_get**
> object api_gdpr_export_get()

Export my personal data (GDPR Art. 15)

Returns the authenticated subject's personal data as a downloadable JSON attachment. Self-scoped — a caller can only export their own data.

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
    api_instance = mudbase.ComplianceApi(api_client)

    try:
        # Export my personal data (GDPR Art. 15)
        api_response = api_instance.api_gdpr_export_get()
        print("The response of ComplianceApi->api_gdpr_export_get:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ComplianceApi->api_gdpr_export_get: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

**object**

### Authorization

[OrgBearerAuth](../README.md#OrgBearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | JSON attachment containing the subject&#39;s personal data |  -  |
**401** | Authentication required |  -  |
**429** | Rate limit exceeded |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **generate_access_review**
> GenerateAccessReview200Response generate_access_review(generate_access_review_request)

Generate access review report (SOC 2)

Generate access review report for compliance audits (SOC 2, ISO 27001, etc.).
Requires JWT Bearer token authentication. Both OrgBearerAuth and ProjectBearerAuth are supported (they use the same JWT token format). These are organization-level operations.


### Example

* Bearer (JWT) Authentication (OrgBearerAuth):
* Bearer (JWT) Authentication (ProjectBearerAuth):

```python
import mudbase
from mudbase.models.generate_access_review200_response import GenerateAccessReview200Response
from mudbase.models.generate_access_review_request import GenerateAccessReviewRequest
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
    api_instance = mudbase.ComplianceApi(api_client)
    generate_access_review_request = {"orgId":"685acbe0e129932fbb7a0fc3","reviewPeriod":{"start":"2024-10-01T00:00:00.000Z","end":"2024-12-31T23:59:59.000Z"}} # GenerateAccessReviewRequest | 

    try:
        # Generate access review report (SOC 2)
        api_response = api_instance.generate_access_review(generate_access_review_request)
        print("The response of ComplianceApi->generate_access_review:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ComplianceApi->generate_access_review: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **generate_access_review_request** | [**GenerateAccessReviewRequest**](GenerateAccessReviewRequest.md)|  | 

### Return type

[**GenerateAccessReview200Response**](GenerateAccessReview200Response.md)

### Authorization

[OrgBearerAuth](../README.md#OrgBearerAuth), [ProjectBearerAuth](../README.md#ProjectBearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Access review report generated |  -  |
**400** | Bad request |  -  |
**401** | Authentication required |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **generate_data_processing_record**
> GenerateDataProcessingRecord200Response generate_data_processing_record(generate_data_processing_record_request)

Generate data processing record (GDPR Article 30)

Generate GDPR Article 30 compliant data processing record

### Example

* Bearer (JWT) Authentication (OrgBearerAuth):
* Bearer (JWT) Authentication (ProjectBearerAuth):

```python
import mudbase
from mudbase.models.generate_data_processing_record200_response import GenerateDataProcessingRecord200Response
from mudbase.models.generate_data_processing_record_request import GenerateDataProcessingRecordRequest
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
    api_instance = mudbase.ComplianceApi(api_client)
    generate_data_processing_record_request = {"orgId":"685acbe0e129932fbb7a0fc3","recordDate":"2024-12-16T00:00:00.000Z"} # GenerateDataProcessingRecordRequest | 

    try:
        # Generate data processing record (GDPR Article 30)
        api_response = api_instance.generate_data_processing_record(generate_data_processing_record_request)
        print("The response of ComplianceApi->generate_data_processing_record:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ComplianceApi->generate_data_processing_record: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **generate_data_processing_record_request** | [**GenerateDataProcessingRecordRequest**](GenerateDataProcessingRecordRequest.md)|  | 

### Return type

[**GenerateDataProcessingRecord200Response**](GenerateDataProcessingRecord200Response.md)

### Authorization

[OrgBearerAuth](../README.md#OrgBearerAuth), [ProjectBearerAuth](../README.md#ProjectBearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Data processing record generated |  -  |
**400** | Bad request |  -  |
**401** | Authentication required |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_compliance_summary**
> GetComplianceSummary200Response get_compliance_summary()

Get compliance summary

Get compliance dashboard data (GDPR, SOC 2, security status). Requires JWT Bearer token authentication. Both OrgBearerAuth and ProjectBearerAuth are supported (they use the same JWT token format). These are organization-level operations.

### Example

* Bearer (JWT) Authentication (OrgBearerAuth):
* Bearer (JWT) Authentication (ProjectBearerAuth):

```python
import mudbase
from mudbase.models.get_compliance_summary200_response import GetComplianceSummary200Response
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
    api_instance = mudbase.ComplianceApi(api_client)

    try:
        # Get compliance summary
        api_response = api_instance.get_compliance_summary()
        print("The response of ComplianceApi->get_compliance_summary:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ComplianceApi->get_compliance_summary: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

[**GetComplianceSummary200Response**](GetComplianceSummary200Response.md)

### Authorization

[OrgBearerAuth](../README.md#OrgBearerAuth), [ProjectBearerAuth](../README.md#ProjectBearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Compliance summary |  -  |
**401** | Authentication required |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **log_security_event**
> LogSecurityEvent200Response log_security_event(log_security_event_request)

Log security event

Log a security event for compliance and audit purposes

### Example

* Bearer (JWT) Authentication (OrgBearerAuth):
* Bearer (JWT) Authentication (ProjectBearerAuth):

```python
import mudbase
from mudbase.models.log_security_event200_response import LogSecurityEvent200Response
from mudbase.models.log_security_event_request import LogSecurityEventRequest
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
    api_instance = mudbase.ComplianceApi(api_client)
    log_security_event_request = {"eventType":"unauthorized_access_attempt","severity":"high","details":{"userId":"685acbe0e129932fbb7a0fc2","resource":"admin-panel","ipAddress":"192.168.1.100","action":"blocked","reason":"Insufficient permissions"}} # LogSecurityEventRequest | 

    try:
        # Log security event
        api_response = api_instance.log_security_event(log_security_event_request)
        print("The response of ComplianceApi->log_security_event:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ComplianceApi->log_security_event: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **log_security_event_request** | [**LogSecurityEventRequest**](LogSecurityEventRequest.md)|  | 

### Return type

[**LogSecurityEvent200Response**](LogSecurityEvent200Response.md)

### Authorization

[OrgBearerAuth](../README.md#OrgBearerAuth), [ProjectBearerAuth](../README.md#ProjectBearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Security event logged |  -  |
**400** | Bad request |  -  |
**401** | Authentication required |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

