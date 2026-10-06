# mudbase.BillingApi

All URIs are relative to *https://cloud.mudbase.dev*

Method | HTTP request | Description
------------- | ------------- | -------------
[**cancel_subscription**](BillingApi.md#cancel_subscription) | **POST** /api/billing/subscriptions/{subscriptionId}/cancel | Cancel subscription
[**check_feature_access**](BillingApi.md#check_feature_access) | **GET** /api/billing/public/projects/{projectId}/feature-access | Check feature access (public)
[**check_subscription**](BillingApi.md#check_subscription) | **GET** /api/billing/public/projects/{projectId}/subscription | Check subscription status (public)
[**create_checkout_session**](BillingApi.md#create_checkout_session) | **POST** /api/billing/public/projects/{projectId}/checkout | Create checkout session (fiat)
[**create_plan**](BillingApi.md#create_plan) | **POST** /api/billing/projects/{projectId}/plans | Create billing plan
[**delete_plan**](BillingApi.md#delete_plan) | **DELETE** /api/billing/projects/{projectId}/plans/{planId} | Delete billing plan
[**download_invoice**](BillingApi.md#download_invoice) | **GET** /api/billing/projects/{projectId}/invoices/{invoiceId}/download | Download invoice PDF
[**enable_payment_processing**](BillingApi.md#enable_payment_processing) | **POST** /api/orgs/{orgId}/payment-processing/enable | Submit payout onboarding for organization
[**export_invoice**](BillingApi.md#export_invoice) | **GET** /api/billing/projects/{projectId}/invoices/{invoiceId}/export | Export invoice (e.g. PDF URL or file)
[**get_billing_estimate**](BillingApi.md#get_billing_estimate) | **GET** /api/billing/estimate | Get billing estimate and forecast
[**get_checkout_payment**](BillingApi.md#get_checkout_payment) | **GET** /api/billing/public/projects/{projectId}/checkout/{paymentId} | Get checkout payment details (not used for fiat billing)
[**get_dashboard**](BillingApi.md#get_dashboard) | **GET** /api/billing/projects/{projectId}/dashboard | Get billing dashboard data
[**get_fee_breakdown**](BillingApi.md#get_fee_breakdown) | **GET** /api/orgs/{orgId}/payment-processing/fee-breakdown | Preview the fee for a given amount
[**get_invoice**](BillingApi.md#get_invoice) | **GET** /api/billing/projects/{projectId}/invoices/{invoiceId} | Get single invoice
[**get_invoices**](BillingApi.md#get_invoices) | **GET** /api/billing/projects/{projectId}/invoices | List project invoices
[**get_payment_processing_status**](BillingApi.md#get_payment_processing_status) | **GET** /api/orgs/{orgId}/payment-processing/status | Get payout-onboarding status for organization
[**get_payment_records**](BillingApi.md#get_payment_records) | **GET** /api/orgs/{orgId}/payment-processing/records | List fiat payment records for organization
[**get_payout_banks**](BillingApi.md#get_payout_banks) | **GET** /api/orgs/{orgId}/payment-processing/banks | List settlement banks for a payout country
[**get_payout_countries**](BillingApi.md#get_payout_countries) | **GET** /api/orgs/{orgId}/payment-processing/countries | List supported payout countries
[**get_plans**](BillingApi.md#get_plans) | **GET** /api/billing/projects/{projectId}/plans | Get billing plans
[**get_public_plans**](BillingApi.md#get_public_plans) | **GET** /api/billing/public/projects/{projectId}/plans | Get public plans (no auth required)
[**get_subscription_tier_by_id**](BillingApi.md#get_subscription_tier_by_id) | **GET** /api/billing/plans/{planId} | Get one subscription tier by id
[**get_subscription_tiers**](BillingApi.md#get_subscription_tiers) | **GET** /api/billing/plans | Get subscription tiers (org-level BaaS plans)
[**get_subscriptions**](BillingApi.md#get_subscriptions) | **GET** /api/billing/projects/{projectId}/subscriptions | Get subscriptions
[**initialize_org_plan_checkout**](BillingApi.md#initialize_org_plan_checkout) | **POST** /api/billing/org/checkout | Initialize org-level BaaS plan payment (Basic, Starter, Growth, Scale)
[**initialize_payment**](BillingApi.md#initialize_payment) | **POST** /api/orgs/{orgId}/payment-processing/initialize-payment | Initialize fiat payment
[**initialize_payment_for_project**](BillingApi.md#initialize_payment_for_project) | **POST** /api/projects/{projectId}/payment-processing/initialize-payment | Initialize fiat payment (project-scoped)
[**record_usage**](BillingApi.md#record_usage) | **POST** /api/billing/public/projects/{projectId}/usage | Record usage (public)
[**update_plan**](BillingApi.md#update_plan) | **PATCH** /api/billing/projects/{projectId}/plans/{planId} | Update billing plan
[**verify_org_plan_payment**](BillingApi.md#verify_org_plan_payment) | **POST** /api/billing/org/verify-payment | Verify org-level plan payment
[**verify_payment**](BillingApi.md#verify_payment) | **POST** /api/billing/public/projects/{projectId}/verify-payment | Verify payment and create subscription


# **cancel_subscription**
> DeleteRole200Response cancel_subscription(subscription_id, cancel_subscription_request=cancel_subscription_request)

Cancel subscription

### Example

* Bearer (JWT) Authentication (OrgBearerAuth):
* Bearer (JWT) Authentication (ProjectBearerAuth):

```python
import mudbase
from mudbase.models.cancel_subscription_request import CancelSubscriptionRequest
from mudbase.models.delete_role200_response import DeleteRole200Response
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
    api_instance = mudbase.BillingApi(api_client)
    subscription_id = 'subscription_id_example' # str | 
    cancel_subscription_request = {"cancelImmediately":false} # CancelSubscriptionRequest |  (optional)

    try:
        # Cancel subscription
        api_response = api_instance.cancel_subscription(subscription_id, cancel_subscription_request=cancel_subscription_request)
        print("The response of BillingApi->cancel_subscription:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling BillingApi->cancel_subscription: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **subscription_id** | **str**|  | 
 **cancel_subscription_request** | [**CancelSubscriptionRequest**](CancelSubscriptionRequest.md)|  | [optional] 

### Return type

[**DeleteRole200Response**](DeleteRole200Response.md)

### Authorization

[OrgBearerAuth](../README.md#OrgBearerAuth), [ProjectBearerAuth](../README.md#ProjectBearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Subscription cancelled |  -  |
**401** | Authentication required |  -  |
**404** | Resource not found |  -  |
**500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **check_feature_access**
> CheckFeatureAccess200Response check_feature_access(project_id, email, feature)

Check feature access (public)

### Example


```python
import mudbase
from mudbase.models.check_feature_access200_response import CheckFeatureAccess200Response
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
    api_instance = mudbase.BillingApi(api_client)
    project_id = 'project_id_example' # str | 
    email = 'email_example' # str | Customer email
    feature = 'feature_example' # str | Feature slug to check access for

    try:
        # Check feature access (public)
        api_response = api_instance.check_feature_access(project_id, email, feature)
        print("The response of BillingApi->check_feature_access:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling BillingApi->check_feature_access: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **str**|  | 
 **email** | **str**| Customer email | 
 **feature** | **str**| Feature slug to check access for | 

### Return type

[**CheckFeatureAccess200Response**](CheckFeatureAccess200Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Feature access status |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **check_subscription**
> CheckSubscription200Response check_subscription(project_id, email)

Check subscription status (public)

### Example


```python
import mudbase
from mudbase.models.check_subscription200_response import CheckSubscription200Response
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
    api_instance = mudbase.BillingApi(api_client)
    project_id = 'project_id_example' # str | 
    email = 'email_example' # str | Customer email to check subscription for

    try:
        # Check subscription status (public)
        api_response = api_instance.check_subscription(project_id, email)
        print("The response of BillingApi->check_subscription:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling BillingApi->check_subscription: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **str**|  | 
 **email** | **str**| Customer email to check subscription for | 

### Return type

[**CheckSubscription200Response**](CheckSubscription200Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Subscription status |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **create_checkout_session**
> CreateCheckoutSession200Response create_checkout_session(project_id, create_checkout_session_request)

Create checkout session (fiat)

**Customer subscription flow — Step 2.** Creates a fiat checkout session. Request body must include planId (from GET public plans), billingCycle (monthly|yearly), and customerInfo.email. Redirect the user to **checkoutUrl** (same URL as authorizationUrl). After payment, call verify-payment with **reference** (mudbase_...).
Response includes only fiat fields (no paymentAddress, paymentOptions, network, asset, or pmt_ references).


### Example


```python
import mudbase
from mudbase.models.create_checkout_session200_response import CreateCheckoutSession200Response
from mudbase.models.create_checkout_session_request import CreateCheckoutSessionRequest
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
    api_instance = mudbase.BillingApi(api_client)
    project_id = 'project_id_example' # str | Project ID
    create_checkout_session_request = {"planId":"65a1b2c3d4e5f6789012345d","billingCycle":"monthly","customerInfo":{"email":"customer@example.com","name":"John Doe"},"successUrl":"https://app.example.com/success","cancelUrl":"https://app.example.com/cancel"} # CreateCheckoutSessionRequest | 

    try:
        # Create checkout session (fiat)
        api_response = api_instance.create_checkout_session(project_id, create_checkout_session_request)
        print("The response of BillingApi->create_checkout_session:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling BillingApi->create_checkout_session: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **str**| Project ID | 
 **create_checkout_session_request** | [**CreateCheckoutSessionRequest**](CreateCheckoutSessionRequest.md)|  | 

### Return type

[**CreateCheckoutSession200Response**](CreateCheckoutSession200Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Checkout session created |  -  |
**400** | Missing planId, billingCycle, or customerInfo.email |  -  |
**500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **create_plan**
> CreatePlan201Response create_plan(project_id, create_plan_request)

Create billing plan

### Example

* Bearer (JWT) Authentication (OrgBearerAuth):
* Bearer (JWT) Authentication (ProjectBearerAuth):

```python
import mudbase
from mudbase.models.create_plan201_response import CreatePlan201Response
from mudbase.models.create_plan_request import CreatePlanRequest
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
    api_instance = mudbase.BillingApi(api_client)
    project_id = 'project_id_example' # str | 
    create_plan_request = {"name":"Pro Plan","description":"Professional plan with advanced features","price":29.99,"currency":"USD","interval":"month","features":["Unlimited API calls","Priority support","Advanced analytics"]} # CreatePlanRequest | 

    try:
        # Create billing plan
        api_response = api_instance.create_plan(project_id, create_plan_request)
        print("The response of BillingApi->create_plan:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling BillingApi->create_plan: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **str**|  | 
 **create_plan_request** | [**CreatePlanRequest**](CreatePlanRequest.md)|  | 

### Return type

[**CreatePlan201Response**](CreatePlan201Response.md)

### Authorization

[OrgBearerAuth](../README.md#OrgBearerAuth), [ProjectBearerAuth](../README.md#ProjectBearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | Plan created |  -  |
**400** | Bad request |  -  |
**401** | Authentication required |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_plan**
> MessageResponse delete_plan(project_id, plan_id)

Delete billing plan

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
    api_instance = mudbase.BillingApi(api_client)
    project_id = 'project_id_example' # str | 
    plan_id = 'plan_id_example' # str | 

    try:
        # Delete billing plan
        api_response = api_instance.delete_plan(project_id, plan_id)
        print("The response of BillingApi->delete_plan:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling BillingApi->delete_plan: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **str**|  | 
 **plan_id** | **str**|  | 

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
**200** | Plan deleted |  -  |
**401** | Authentication required |  -  |
**404** | Resource not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **download_invoice**
> bytearray download_invoice(project_id, invoice_id)

Download invoice PDF

### Example

* Bearer (JWT) Authentication (OrgBearerAuth):
* Bearer (JWT) Authentication (ProjectBearerAuth):

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

# Configure Bearer authorization (JWT): ProjectBearerAuth
configuration = mudbase.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with mudbase.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = mudbase.BillingApi(api_client)
    project_id = 'project_id_example' # str | 
    invoice_id = 'invoice_id_example' # str | 

    try:
        # Download invoice PDF
        api_response = api_instance.download_invoice(project_id, invoice_id)
        print("The response of BillingApi->download_invoice:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling BillingApi->download_invoice: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **str**|  | 
 **invoice_id** | **str**|  | 

### Return type

**bytearray**

### Authorization

[OrgBearerAuth](../README.md#OrgBearerAuth), [ProjectBearerAuth](../README.md#ProjectBearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/pdf, application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Invoice PDF file or redirect URL |  -  |
**401** | Authentication required |  -  |
**404** | Invoice not found |  -  |
**500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **enable_payment_processing**
> EnablePaymentProcessing200Response enable_payment_processing(org_id, enable_payment_processing_request)

Submit payout onboarding for organization

Validates and stores the org's payout account details, then queues the org for platform-admin review. This does not activate payments by itself; initialize-payment only starts succeeding once the org is approved. The required fields depend on the chosen country: call GET /payment-processing/countries first and collect exactly the fields that country's schema returns (bank code + account number for most African markets, plus a BVN for Nigeria, or routing number/sort code + account type + account holder name for the US/UK). Requires owner or admin role.

### Example

* Bearer (JWT) Authentication (OrgBearerAuth):

```python
import mudbase
from mudbase.models.enable_payment_processing200_response import EnablePaymentProcessing200Response
from mudbase.models.enable_payment_processing_request import EnablePaymentProcessingRequest
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
    api_instance = mudbase.BillingApi(api_client)
    org_id = 'org_id_example' # str | 
    enable_payment_processing_request = {"country":"NG","businessName":"Acme Inc","accountBank":"044","accountNumber":"0123456789","bvn":"12345678901"} # EnablePaymentProcessingRequest | 

    try:
        # Submit payout onboarding for organization
        api_response = api_instance.enable_payment_processing(org_id, enable_payment_processing_request)
        print("The response of BillingApi->enable_payment_processing:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling BillingApi->enable_payment_processing: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**|  | 
 **enable_payment_processing_request** | [**EnablePaymentProcessingRequest**](EnablePaymentProcessingRequest.md)|  | 

### Return type

[**EnablePaymentProcessing200Response**](EnablePaymentProcessing200Response.md)

### Authorization

[OrgBearerAuth](../README.md#OrgBearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Onboarding submitted (or already enabled) |  -  |
**400** | Bad request |  -  |
**401** | Authentication required |  -  |
**403** | Access denied |  -  |
**500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **export_invoice**
> DownloadInvoice200Response export_invoice(project_id, invoice_id)

Export invoice (e.g. PDF URL or file)

### Example

* Bearer (JWT) Authentication (OrgBearerAuth):
* Bearer (JWT) Authentication (ProjectBearerAuth):

```python
import mudbase
from mudbase.models.download_invoice200_response import DownloadInvoice200Response
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
    api_instance = mudbase.BillingApi(api_client)
    project_id = 'project_id_example' # str | 
    invoice_id = 'invoice_id_example' # str | 

    try:
        # Export invoice (e.g. PDF URL or file)
        api_response = api_instance.export_invoice(project_id, invoice_id)
        print("The response of BillingApi->export_invoice:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling BillingApi->export_invoice: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **str**|  | 
 **invoice_id** | **str**|  | 

### Return type

[**DownloadInvoice200Response**](DownloadInvoice200Response.md)

### Authorization

[OrgBearerAuth](../README.md#OrgBearerAuth), [ProjectBearerAuth](../README.md#ProjectBearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Export result (URL or file) |  -  |
**401** | Authentication required |  -  |
**404** | Invoice not found |  -  |
**500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_billing_estimate**
> GetBillingEstimate200Response get_billing_estimate()

Get billing estimate and forecast

Returns current-month overage estimate and an optional end-of-month forecast for the authenticated organization.
Includes spend limit settings (soft/hard) and whether usage is currently blocked. Requires org-level JWT.


### Example

* Bearer (JWT) Authentication (OrgBearerAuth):

```python
import mudbase
from mudbase.models.get_billing_estimate200_response import GetBillingEstimate200Response
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
    api_instance = mudbase.BillingApi(api_client)

    try:
        # Get billing estimate and forecast
        api_response = api_instance.get_billing_estimate()
        print("The response of BillingApi->get_billing_estimate:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling BillingApi->get_billing_estimate: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

[**GetBillingEstimate200Response**](GetBillingEstimate200Response.md)

### Authorization

[OrgBearerAuth](../README.md#OrgBearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Billing estimate and forecast |  -  |
**401** | Authentication required |  -  |
**503** | Service temporarily unavailable. Returned when the organization is restricted (e.g. suspended due to unpaid overage, spend limit exceeded, or API usage limit reached). End-users see a generic message; the real reason is logged server-side only.  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_checkout_payment**
> get_checkout_payment(project_id, payment_id)

Get checkout payment details (not used for fiat billing)

**Fiat-only billing:** checkout is completed on the payment gateway's hosted page; there is no server-side payment intent to poll.
The live API returns **404** for this route. Reserved for compatibility; do not rely on a success body for project billing.


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
    api_instance = mudbase.BillingApi(api_client)
    project_id = 'project_id_example' # str | 
    payment_id = 'payment_id_example' # str | Opaque id from checkout (fiat billing does not expose pollable payment state here)

    try:
        # Get checkout payment details (not used for fiat billing)
        api_instance.get_checkout_payment(project_id, payment_id)
    except Exception as e:
        print("Exception when calling BillingApi->get_checkout_payment: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **str**|  | 
 **payment_id** | **str**| Opaque id from checkout (fiat billing does not expose pollable payment state here) | 

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
**404** | Payment not found |  -  |
**500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_dashboard**
> GetDashboard200Response get_dashboard(project_id)

Get billing dashboard data

### Example

* Bearer (JWT) Authentication (OrgBearerAuth):
* Bearer (JWT) Authentication (ProjectBearerAuth):

```python
import mudbase
from mudbase.models.get_dashboard200_response import GetDashboard200Response
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
    api_instance = mudbase.BillingApi(api_client)
    project_id = 'project_id_example' # str | 

    try:
        # Get billing dashboard data
        api_response = api_instance.get_dashboard(project_id)
        print("The response of BillingApi->get_dashboard:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling BillingApi->get_dashboard: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **str**|  | 

### Return type

[**GetDashboard200Response**](GetDashboard200Response.md)

### Authorization

[OrgBearerAuth](../README.md#OrgBearerAuth), [ProjectBearerAuth](../README.md#ProjectBearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Dashboard data |  -  |
**401** | Authentication required |  -  |
**404** | Project not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_fee_breakdown**
> GetFeeBreakdown200Response get_fee_breakdown(org_id, amount, currency=currency, country=country, method=method, international=international)

Preview the fee for a given amount

Returns the single all-in Mudbase fee, its effective rate, and what the org would net for the given amount, without creating a payment. Pass country/method/international to price a specific rail; omitting them uses a generic local-rail estimate. Never returns the underlying rail's own cost or any internal margin split.

### Example

* Bearer (JWT) Authentication (OrgBearerAuth):

```python
import mudbase
from mudbase.models.get_fee_breakdown200_response import GetFeeBreakdown200Response
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
    api_instance = mudbase.BillingApi(api_client)
    org_id = 'org_id_example' # str | 
    amount = 3.4 # float | 
    currency = 'USD' # str |  (optional) (default to 'USD')
    country = 'country_example' # str | ISO-3166 alpha-2 payout country code, one of the codes from GET /payment-processing/countries. (optional)
    method = card # str |  (optional) (default to card)
    international = False # bool | Set true for a cross-border/international card, Apple Pay, or Google Pay. (optional) (default to False)

    try:
        # Preview the fee for a given amount
        api_response = api_instance.get_fee_breakdown(org_id, amount, currency=currency, country=country, method=method, international=international)
        print("The response of BillingApi->get_fee_breakdown:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling BillingApi->get_fee_breakdown: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**|  | 
 **amount** | **float**|  | 
 **currency** | **str**|  | [optional] [default to &#39;USD&#39;]
 **country** | **str**| ISO-3166 alpha-2 payout country code, one of the codes from GET /payment-processing/countries. | [optional] 
 **method** | **str**|  | [optional] [default to card]
 **international** | **bool**| Set true for a cross-border/international card, Apple Pay, or Google Pay. | [optional] [default to False]

### Return type

[**GetFeeBreakdown200Response**](GetFeeBreakdown200Response.md)

### Authorization

[OrgBearerAuth](../README.md#OrgBearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Fee breakdown |  -  |
**400** | Bad request |  -  |
**401** | Authentication required |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_invoice**
> GetInvoice200Response get_invoice(project_id, invoice_id)

Get single invoice

### Example

* Bearer (JWT) Authentication (OrgBearerAuth):
* Bearer (JWT) Authentication (ProjectBearerAuth):

```python
import mudbase
from mudbase.models.get_invoice200_response import GetInvoice200Response
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
    api_instance = mudbase.BillingApi(api_client)
    project_id = 'project_id_example' # str | 
    invoice_id = 'invoice_id_example' # str | 

    try:
        # Get single invoice
        api_response = api_instance.get_invoice(project_id, invoice_id)
        print("The response of BillingApi->get_invoice:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling BillingApi->get_invoice: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **str**|  | 
 **invoice_id** | **str**|  | 

### Return type

[**GetInvoice200Response**](GetInvoice200Response.md)

### Authorization

[OrgBearerAuth](../README.md#OrgBearerAuth), [ProjectBearerAuth](../README.md#ProjectBearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Invoice details |  -  |
**401** | Authentication required |  -  |
**404** | Invoice not found |  -  |
**500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_invoices**
> GetInvoices200Response get_invoices(project_id)

List project invoices

### Example

* Bearer (JWT) Authentication (OrgBearerAuth):
* Bearer (JWT) Authentication (ProjectBearerAuth):

```python
import mudbase
from mudbase.models.get_invoices200_response import GetInvoices200Response
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
    api_instance = mudbase.BillingApi(api_client)
    project_id = 'project_id_example' # str | 

    try:
        # List project invoices
        api_response = api_instance.get_invoices(project_id)
        print("The response of BillingApi->get_invoices:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling BillingApi->get_invoices: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **str**|  | 

### Return type

[**GetInvoices200Response**](GetInvoices200Response.md)

### Authorization

[OrgBearerAuth](../README.md#OrgBearerAuth), [ProjectBearerAuth](../README.md#ProjectBearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Invoices list |  -  |
**401** | Authentication required |  -  |
**500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_payment_processing_status**
> GetPaymentProcessingStatus200Response get_payment_processing_status(org_id)

Get payout-onboarding status for organization

Returns the current onboarding/approval state for the org's payout account. Poll this after calling enable, or before calling initialize-payment, to confirm the org is actually approved rather than assuming a 200 from enable means payments are live. Never returns the raw payout-account id, only whether one exists.

### Example

* Bearer (JWT) Authentication (OrgBearerAuth):

```python
import mudbase
from mudbase.models.get_payment_processing_status200_response import GetPaymentProcessingStatus200Response
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
    api_instance = mudbase.BillingApi(api_client)
    org_id = 'org_id_example' # str | 

    try:
        # Get payout-onboarding status for organization
        api_response = api_instance.get_payment_processing_status(org_id)
        print("The response of BillingApi->get_payment_processing_status:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling BillingApi->get_payment_processing_status: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**|  | 

### Return type

[**GetPaymentProcessingStatus200Response**](GetPaymentProcessingStatus200Response.md)

### Authorization

[OrgBearerAuth](../README.md#OrgBearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Payout-onboarding status |  -  |
**401** | Authentication required |  -  |
**403** | Access denied |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_payment_records**
> GetPaymentRecords200Response get_payment_records(org_id, page=page, limit=limit, status=status)

List fiat payment records for organization

Paginated list of FiatPaymentRecord for this org (txRef, amount, orgReceives, status, paidAt).

### Example

* Bearer (JWT) Authentication (OrgBearerAuth):

```python
import mudbase
from mudbase.models.get_payment_records200_response import GetPaymentRecords200Response
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
    api_instance = mudbase.BillingApi(api_client)
    org_id = 'org_id_example' # str | 
    page = 1 # int |  (optional) (default to 1)
    limit = 20 # int |  (optional) (default to 20)
    status = 'status_example' # str |  (optional)

    try:
        # List fiat payment records for organization
        api_response = api_instance.get_payment_records(org_id, page=page, limit=limit, status=status)
        print("The response of BillingApi->get_payment_records:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling BillingApi->get_payment_records: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**|  | 
 **page** | **int**|  | [optional] [default to 1]
 **limit** | **int**|  | [optional] [default to 20]
 **status** | **str**|  | [optional] 

### Return type

[**GetPaymentRecords200Response**](GetPaymentRecords200Response.md)

### Authorization

[OrgBearerAuth](../README.md#OrgBearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Records and pagination |  -  |
**401** | Authentication required |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_payout_banks**
> GetPayoutBanks200Response get_payout_banks(org_id, country)

List settlement banks for a payout country

Read-only lookup of the settlement-bank list for a country, only meaningful when that country's entry from GET /payment-processing/countries has banksListSupported: true. For a country where it is false, this returns an empty list and your onboarding form should fall back to the free-text bank/code field the countries response already describes for that country, rather than calling this endpoint.

### Example

* Bearer (JWT) Authentication (OrgBearerAuth):

```python
import mudbase
from mudbase.models.get_payout_banks200_response import GetPayoutBanks200Response
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
    api_instance = mudbase.BillingApi(api_client)
    org_id = 'org_id_example' # str | 
    country = 'country_example' # str | ISO-3166 alpha-2 payout country code, one of the codes from GET /payment-processing/countries.

    try:
        # List settlement banks for a payout country
        api_response = api_instance.get_payout_banks(org_id, country)
        print("The response of BillingApi->get_payout_banks:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling BillingApi->get_payout_banks: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**|  | 
 **country** | **str**| ISO-3166 alpha-2 payout country code, one of the codes from GET /payment-processing/countries. | 

### Return type

[**GetPayoutBanks200Response**](GetPayoutBanks200Response.md)

### Authorization

[OrgBearerAuth](../README.md#OrgBearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Bank list for the country |  -  |
**400** | Bad request |  -  |
**401** | Authentication required |  -  |
**403** | Access denied |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_payout_countries**
> GetPayoutCountries200Response get_payout_countries(org_id)

List supported payout countries

Returns the full supported payout-country set and each country's payout-account field schema. Drives a dynamic onboarding form: which fields to collect (bank code/routing number/sort code/IBAN, whether a BVN is required, whether a bank list or mobile-money network applies) comes straight from this response, so build your onboarding UI to render from it rather than hardcoding a country list.

### Example

* Bearer (JWT) Authentication (OrgBearerAuth):

```python
import mudbase
from mudbase.models.get_payout_countries200_response import GetPayoutCountries200Response
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
    api_instance = mudbase.BillingApi(api_client)
    org_id = 'org_id_example' # str | 

    try:
        # List supported payout countries
        api_response = api_instance.get_payout_countries(org_id)
        print("The response of BillingApi->get_payout_countries:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling BillingApi->get_payout_countries: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**|  | 

### Return type

[**GetPayoutCountries200Response**](GetPayoutCountries200Response.md)

### Authorization

[OrgBearerAuth](../README.md#OrgBearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Supported countries and field schemas |  -  |
**401** | Authentication required |  -  |
**403** | Access denied |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_plans**
> GetPlans200Response get_plans(project_id)

Get billing plans

### Example

* Bearer (JWT) Authentication (OrgBearerAuth):
* Bearer (JWT) Authentication (ProjectBearerAuth):

```python
import mudbase
from mudbase.models.get_plans200_response import GetPlans200Response
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
    api_instance = mudbase.BillingApi(api_client)
    project_id = 'project_id_example' # str | 

    try:
        # Get billing plans
        api_response = api_instance.get_plans(project_id)
        print("The response of BillingApi->get_plans:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling BillingApi->get_plans: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **str**|  | 

### Return type

[**GetPlans200Response**](GetPlans200Response.md)

### Authorization

[OrgBearerAuth](../README.md#OrgBearerAuth), [ProjectBearerAuth](../README.md#ProjectBearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Plans list |  -  |
**401** | Authentication required |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_public_plans**
> GetPublicPlans200Response get_public_plans(project_id)

Get public plans (no auth required)

**Customer subscription flow — Step 1.** Returns all active plans for the project. Use a plan's _id as planId in the checkout request. No authentication required (for pricing/checkout pages).


### Example


```python
import mudbase
from mudbase.models.get_public_plans200_response import GetPublicPlans200Response
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
    api_instance = mudbase.BillingApi(api_client)
    project_id = 'project_id_example' # str | 

    try:
        # Get public plans (no auth required)
        api_response = api_instance.get_public_plans(project_id)
        print("The response of BillingApi->get_public_plans:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling BillingApi->get_public_plans: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **str**|  | 

### Return type

[**GetPublicPlans200Response**](GetPublicPlans200Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Public plans list |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_subscription_tier_by_id**
> GetSubscriptionTierById200Response get_subscription_tier_by_id(plan_id)

Get one subscription tier by id

Returns a single org-level BaaS plan (free, basic, starter, growth, scale, enterprise). Public; no auth required.

### Example


```python
import mudbase
from mudbase.models.get_subscription_tier_by_id200_response import GetSubscriptionTierById200Response
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
    api_instance = mudbase.BillingApi(api_client)
    plan_id = 'plan_id_example' # str | Plan id (free, basic, starter, growth, scale, enterprise)

    try:
        # Get one subscription tier by id
        api_response = api_instance.get_subscription_tier_by_id(plan_id)
        print("The response of BillingApi->get_subscription_tier_by_id:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling BillingApi->get_subscription_tier_by_id: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **plan_id** | **str**| Plan id (free, basic, starter, growth, scale, enterprise) | 

### Return type

[**GetSubscriptionTierById200Response**](GetSubscriptionTierById200Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Plan details |  -  |
**404** | Plan not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_subscription_tiers**
> GetSubscriptionTiers200Response get_subscription_tiers()

Get subscription tiers (org-level BaaS plans)

**Org-level BaaS plan catalog** (source of truth in paymentService.js). Returns Free, Basic ($12), Starter ($29), Growth ($69), Scale ($199), Enterprise. Use for pricing page and to get plan ids for POST /api/billing/org/checkout. Public; no auth required.
Each plan includes id (free|basic|starter|growth|scale|enterprise), name, description, price (cents), priceYearly (cents, 2 months free), currency, limits, overages, enforcement.


### Example


```python
import mudbase
from mudbase.models.get_subscription_tiers200_response import GetSubscriptionTiers200Response
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
    api_instance = mudbase.BillingApi(api_client)

    try:
        # Get subscription tiers (org-level BaaS plans)
        api_response = api_instance.get_subscription_tiers()
        print("The response of BillingApi->get_subscription_tiers:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling BillingApi->get_subscription_tiers: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

[**GetSubscriptionTiers200Response**](GetSubscriptionTiers200Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Plan list |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_subscriptions**
> GetSubscriptions200Response get_subscriptions(project_id)

Get subscriptions

### Example

* Bearer (JWT) Authentication (OrgBearerAuth):
* Bearer (JWT) Authentication (ProjectBearerAuth):

```python
import mudbase
from mudbase.models.get_subscriptions200_response import GetSubscriptions200Response
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
    api_instance = mudbase.BillingApi(api_client)
    project_id = 'project_id_example' # str | 

    try:
        # Get subscriptions
        api_response = api_instance.get_subscriptions(project_id)
        print("The response of BillingApi->get_subscriptions:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling BillingApi->get_subscriptions: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **str**|  | 

### Return type

[**GetSubscriptions200Response**](GetSubscriptions200Response.md)

### Authorization

[OrgBearerAuth](../README.md#OrgBearerAuth), [ProjectBearerAuth](../README.md#ProjectBearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Subscriptions list |  -  |
**401** | Authentication required |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **initialize_org_plan_checkout**
> InitializeOrgPlanCheckout200Response initialize_org_plan_checkout(initialize_org_plan_checkout_request)

Initialize org-level BaaS plan payment (Basic, Starter, Growth, Scale)

**Org plan payment flow — Step 2.** Creates a payment link for the authenticated org to subscribe to a BaaS plan (basic, starter, growth, scale). Enterprise has no price; use contact-sales flow. Redirect the user to the returned link; after payment, call POST /api/billing/org/verify-payment with the tx_ref from the redirect. Requires org-level JWT.


### Example

* Bearer (JWT) Authentication (OrgBearerAuth):

```python
import mudbase
from mudbase.models.initialize_org_plan_checkout200_response import InitializeOrgPlanCheckout200Response
from mudbase.models.initialize_org_plan_checkout_request import InitializeOrgPlanCheckoutRequest
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
    api_instance = mudbase.BillingApi(api_client)
    initialize_org_plan_checkout_request = {"planName":"starter","billingCycle":"monthly"} # InitializeOrgPlanCheckoutRequest | 

    try:
        # Initialize org-level BaaS plan payment (Basic, Starter, Growth, Scale)
        api_response = api_instance.initialize_org_plan_checkout(initialize_org_plan_checkout_request)
        print("The response of BillingApi->initialize_org_plan_checkout:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling BillingApi->initialize_org_plan_checkout: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **initialize_org_plan_checkout_request** | [**InitializeOrgPlanCheckoutRequest**](InitializeOrgPlanCheckoutRequest.md)|  | 

### Return type

[**InitializeOrgPlanCheckout200Response**](InitializeOrgPlanCheckout200Response.md)

### Authorization

[OrgBearerAuth](../README.md#OrgBearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Payment link created |  -  |
**400** | Invalid planName or payment gateway not configured |  -  |
**401** | Organization context required |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **initialize_payment**
> InitializePayment200Response initialize_payment(org_id, initialize_payment_request)

Initialize fiat payment

Creates a payment link. The customer pays; Mudbase charges a single all-in, cost-plus fee (see GET /payment-processing/fee-breakdown for the exact rate for a given country/method) and the org receives the remainder. Requires payment processing enabled and approved for the org.

### Example

* Bearer (JWT) Authentication (OrgBearerAuth):

```python
import mudbase
from mudbase.models.initialize_payment200_response import InitializePayment200Response
from mudbase.models.initialize_payment_request import InitializePaymentRequest
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
    api_instance = mudbase.BillingApi(api_client)
    org_id = 'org_id_example' # str | 
    initialize_payment_request = {"amount":100,"currency":"USD","customer":{"email":"buyer@example.com","name":"Buyer Name"},"metadata":{"title":"Order #123","description":"Payment for order"}} # InitializePaymentRequest | 

    try:
        # Initialize fiat payment
        api_response = api_instance.initialize_payment(org_id, initialize_payment_request)
        print("The response of BillingApi->initialize_payment:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling BillingApi->initialize_payment: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**|  | 
 **initialize_payment_request** | [**InitializePaymentRequest**](InitializePaymentRequest.md)|  | 

### Return type

[**InitializePayment200Response**](InitializePayment200Response.md)

### Authorization

[OrgBearerAuth](../README.md#OrgBearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Payment link and fee breakdown |  -  |
**400** | Bad request |  -  |
**401** | Authentication required |  -  |
**500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **initialize_payment_for_project**
> initialize_payment_for_project(project_id, initialize_payment_for_project_request)

Initialize fiat payment (project-scoped)

Same as org-level initialize-payment; projectId from path is used for scope and tx_ref. Resolves project to org and uses org's payment-processing subaccount.

### Example

* Bearer (JWT) Authentication (OrgBearerAuth):
* Bearer (JWT) Authentication (ProjectBearerAuth):

```python
import mudbase
from mudbase.models.initialize_payment_for_project_request import InitializePaymentForProjectRequest
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
    api_instance = mudbase.BillingApi(api_client)
    project_id = 'project_id_example' # str | 
    initialize_payment_for_project_request = {"amount":0.01,"customer":{"email":"email_example"}} # InitializePaymentForProjectRequest | 

    try:
        # Initialize fiat payment (project-scoped)
        api_instance.initialize_payment_for_project(project_id, initialize_payment_for_project_request)
    except Exception as e:
        print("Exception when calling BillingApi->initialize_payment_for_project: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **str**|  | 
 **initialize_payment_for_project_request** | [**InitializePaymentForProjectRequest**](InitializePaymentForProjectRequest.md)|  | 

### Return type

void (empty response body)

### Authorization

[OrgBearerAuth](../README.md#OrgBearerAuth), [ProjectBearerAuth](../README.md#ProjectBearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Payment link and fee breakdown (same shape as org-level) |  -  |
**400** | Bad request |  -  |
**401** | Authentication required |  -  |
**500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **record_usage**
> MessageResponse record_usage(project_id, record_usage_request)

Record usage (public)

### Example


```python
import mudbase
from mudbase.models.message_response import MessageResponse
from mudbase.models.record_usage_request import RecordUsageRequest
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
    api_instance = mudbase.BillingApi(api_client)
    project_id = 'project_id_example' # str | 
    record_usage_request = {"email":"customer@example.com","metric":"api_calls","quantity":150} # RecordUsageRequest | 

    try:
        # Record usage (public)
        api_response = api_instance.record_usage(project_id, record_usage_request)
        print("The response of BillingApi->record_usage:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling BillingApi->record_usage: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **str**|  | 
 **record_usage_request** | [**RecordUsageRequest**](RecordUsageRequest.md)|  | 

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
**200** | Usage recorded |  -  |
**400** | Bad request |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_plan**
> CreatePlan201Response update_plan(project_id, plan_id, update_plan_request)

Update billing plan

### Example

* Bearer (JWT) Authentication (OrgBearerAuth):
* Bearer (JWT) Authentication (ProjectBearerAuth):

```python
import mudbase
from mudbase.models.create_plan201_response import CreatePlan201Response
from mudbase.models.update_plan_request import UpdatePlanRequest
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
    api_instance = mudbase.BillingApi(api_client)
    project_id = 'project_id_example' # str | 
    plan_id = 'plan_id_example' # str | 
    update_plan_request = {"name":"Pro Plan Updated","description":"Updated professional plan","price":39.99,"features":["Unlimited API calls","Priority support","Advanced analytics"]} # UpdatePlanRequest | 

    try:
        # Update billing plan
        api_response = api_instance.update_plan(project_id, plan_id, update_plan_request)
        print("The response of BillingApi->update_plan:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling BillingApi->update_plan: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **str**|  | 
 **plan_id** | **str**|  | 
 **update_plan_request** | [**UpdatePlanRequest**](UpdatePlanRequest.md)|  | 

### Return type

[**CreatePlan201Response**](CreatePlan201Response.md)

### Authorization

[OrgBearerAuth](../README.md#OrgBearerAuth), [ProjectBearerAuth](../README.md#ProjectBearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Plan updated |  -  |
**400** | Bad request |  -  |
**401** | Authentication required |  -  |
**404** | Resource not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **verify_org_plan_payment**
> VerifyOrgPlanPayment200Response verify_org_plan_payment(tx_ref=tx_ref, reference=reference)

Verify org-level plan payment

**Org plan payment flow — Step 3.** Call after the user completes payment (redirect or webhook). Pass tx_ref (or reference) from the payment redirect. Updates org plan and billing; idempotent. No auth required (redirect callback can call this).


### Example


```python
import mudbase
from mudbase.models.verify_org_plan_payment200_response import VerifyOrgPlanPayment200Response
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
    api_instance = mudbase.BillingApi(api_client)
    tx_ref = 'tx_ref_example' # str | Payment reference (mudbase_org_...) from checkout redirect (optional)
    reference = 'reference_example' # str | Alias for tx_ref (optional)

    try:
        # Verify org-level plan payment
        api_response = api_instance.verify_org_plan_payment(tx_ref=tx_ref, reference=reference)
        print("The response of BillingApi->verify_org_plan_payment:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling BillingApi->verify_org_plan_payment: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **tx_ref** | **str**| Payment reference (mudbase_org_...) from checkout redirect | [optional] 
 **reference** | **str**| Alias for tx_ref | [optional] 

### Return type

[**VerifyOrgPlanPayment200Response**](VerifyOrgPlanPayment200Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Payment verified and org plan updated |  -  |
**400** | tx_ref required, invalid reference, or payment verification failed |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **verify_payment**
> VerifyPayment200Response verify_payment(project_id, reference)

Verify payment and create subscription

**Customer subscription flow — Step 3.** Call after the user completes payment. Pass **reference** as query (?reference=mudbase_...). On success, a subscription is created. No auth required when using the platform gateway (mudbase_ refs). Org-level gateway verification may require JWT. References starting with pmt_ are rejected (crypto billing is not enabled on this API).


### Example


```python
import mudbase
from mudbase.models.verify_payment200_response import VerifyPayment200Response
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
    api_instance = mudbase.BillingApi(api_client)
    project_id = 'project_id_example' # str | 
    reference = 'reference_example' # str | Payment transaction reference (mudbase_...)

    try:
        # Verify payment and create subscription
        api_response = api_instance.verify_payment(project_id, reference)
        print("The response of BillingApi->verify_payment:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling BillingApi->verify_payment: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **str**|  | 
 **reference** | **str**| Payment transaction reference (mudbase_...) | 

### Return type

[**VerifyPayment200Response**](VerifyPayment200Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Payment verified and subscription created |  -  |
**400** | reference is required or organization context missing |  -  |
**403** | Payment does not belong to your organization |  -  |
**500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

