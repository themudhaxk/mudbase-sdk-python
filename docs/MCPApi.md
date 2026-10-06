# mudbase.MCPApi

All URIs are relative to *https://cloud.mudbase.dev*

Method | HTTP request | Description
------------- | ------------- | -------------
[**mcp_config_get**](MCPApi.md#mcp_config_get) | **GET** /mcp/config | MCP connection status for the current org


# **mcp_config_get**
> McpConfigGet200Response mcp_config_get()

MCP connection status for the current org

Whether the org's plan includes MCP access and, when enabled, the endpoint URL an MCP client should connect to (the org's dedicated API host if it has dedicated infrastructure, otherwise the shared platform host). Auth here is the normal dashboard session - this powers the console's MCP settings page, distinct from the API-key-authenticated POST / endpoint an actual MCP client calls.

### Example

* Bearer (JWT) Authentication (OrgBearerAuth):

```python
import mudbase
from mudbase.models.mcp_config_get200_response import McpConfigGet200Response
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
    api_instance = mudbase.MCPApi(api_client)

    try:
        # MCP connection status for the current org
        api_response = api_instance.mcp_config_get()
        print("The response of MCPApi->mcp_config_get:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling MCPApi->mcp_config_get: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

[**McpConfigGet200Response**](McpConfigGet200Response.md)

### Authorization

[OrgBearerAuth](../README.md#OrgBearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | MCP status for the current org |  -  |
**401** | Authentication required |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

