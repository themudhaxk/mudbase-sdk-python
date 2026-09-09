# mudbase.VerifiedRoleUpgradeApi

All URIs are relative to *https://cloud.mudbase.dev*

Method | HTTP request | Description
------------- | ------------- | -------------
[**verified_role_upgrade**](VerifiedRoleUpgradeApi.md#verified_role_upgrade) | **POST** /api/orgs/{orgId}/users/{userId}/upgrade | Verified role upgrade with payment verification


# **verified_role_upgrade**
> VerifiedRoleUpgrade200Response verified_role_upgrade(org_id, user_id, verified_role_upgrade_request)

Verified role upgrade with payment verification

Upgrade user role after verifying payment and KYC. Prevents replay attacks.

### Example

* Bearer (JWT) Authentication (OrgBearerAuth):
* Bearer (JWT) Authentication (ProjectBearerAuth):

```python
import mudbase
from mudbase.models.verified_role_upgrade200_response import VerifiedRoleUpgrade200Response
from mudbase.models.verified_role_upgrade_request import VerifiedRoleUpgradeRequest
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
    api_instance = mudbase.VerifiedRoleUpgradeApi(api_client)
    org_id = 'org_id_example' # str | 
    user_id = 'user_id_example' # str | 
    verified_role_upgrade_request = {"targetRole":"seller","paymentIntentId":"pi_abc123","verificationId":"kyc_xyz789"} # VerifiedRoleUpgradeRequest | 

    try:
        # Verified role upgrade with payment verification
        api_response = api_instance.verified_role_upgrade(org_id, user_id, verified_role_upgrade_request)
        print("The response of VerifiedRoleUpgradeApi->verified_role_upgrade:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling VerifiedRoleUpgradeApi->verified_role_upgrade: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org_id** | **str**|  | 
 **user_id** | **str**|  | 
 **verified_role_upgrade_request** | [**VerifiedRoleUpgradeRequest**](VerifiedRoleUpgradeRequest.md)|  | 

### Return type

[**VerifiedRoleUpgrade200Response**](VerifiedRoleUpgrade200Response.md)

### Authorization

[OrgBearerAuth](../README.md#OrgBearerAuth), [ProjectBearerAuth](../README.md#ProjectBearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Role upgraded successfully |  -  |
**403** | Payment verification failed or insufficient permissions |  -  |
**404** | User or role not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

