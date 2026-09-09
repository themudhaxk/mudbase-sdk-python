# mudbase.FilesApi

All URIs are relative to *https://cloud.mudbase.dev*

Method | HTTP request | Description
------------- | ------------- | -------------
[**api_files_download_file_id_get**](FilesApi.md#api_files_download_file_id_get) | **GET** /api/files/download/{fileId} | Get a download URL for a file
[**api_files_logo_redirect_get**](FilesApi.md#api_files_logo_redirect_get) | **GET** /api/files/logo-redirect | Redirect to an org/project logo&#39;s content
[**api_files_public_file_id_get**](FilesApi.md#api_files_public_file_id_get) | **GET** /api/files/public/{fileId} | Redirect to a public file&#39;s content
[**confirm_direct_upload**](FilesApi.md#confirm_direct_upload) | **POST** /api/files/upload/confirm | Confirm direct upload (scan + finalize metadata)
[**delete_file**](FilesApi.md#delete_file) | **DELETE** /api/bucket/projects/{projectId}/buckets/{bucketId}/files/{fileId} | Delete file
[**download_bucket_file**](FilesApi.md#download_bucket_file) | **GET** /api/bucket/files/{fileId}/download | Download file from bucket
[**download_file**](FilesApi.md#download_file) | **GET** /api/files/{fileId}/download | Generate a presigned URL for downloading a file
[**generate_presigned_upload**](FilesApi.md#generate_presigned_upload) | **POST** /api/files/upload/presigned | Generate a presigned PUT URL for direct browser upload
[**generate_signed_url**](FilesApi.md#generate_signed_url) | **POST** /api/bucket/projects/{projectId}/buckets/{bucketId}/files/{fileId}/signed-url | Generate signed URL for file
[**get_file**](FilesApi.md#get_file) | **GET** /api/bucket/projects/{projectId}/buckets/{bucketId}/files/{fileId} | Get file metadata
[**list_files**](FilesApi.md#list_files) | **GET** /api/bucket/projects/{projectId}/buckets/{bucketId}/files | List files in bucket
[**upload_files**](FilesApi.md#upload_files) | **POST** /api/bucket/projects/{projectId}/buckets/{bucketId}/files | Upload files to bucket


# **api_files_download_file_id_get**
> ApiFilesDownloadFileIdGet200Response api_files_download_file_id_get(file_id, expires_in=expires_in)

Get a download URL for a file

Returns a URL to download the file. For private files a short-lived signed URL is generated; the lifetime can be tuned per request via the optional expiresIn query parameter (seconds, clamped to a safe server-configured range). For public (public-read) files the permanent world-readable URL is returned with isPublic true and a warning, since signing a public object provides no protection. Accepts a JWT (Bearer) or a project API key.

### Example

* Api Key Authentication (ApiKeyAuth):
* Bearer (JWT) Authentication (ProjectBearerAuth):

```python
import mudbase
from mudbase.models.api_files_download_file_id_get200_response import ApiFilesDownloadFileIdGet200Response
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

# Configure API key authorization: ApiKeyAuth
configuration.api_key['ApiKeyAuth'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['ApiKeyAuth'] = 'Bearer'

# Configure Bearer authorization (JWT): ProjectBearerAuth
configuration = mudbase.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with mudbase.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = mudbase.FilesApi(api_client)
    file_id = 'file_id_example' # str | 
    expires_in = 56 # int | Signed-URL lifetime in seconds for private files. Clamped to the server's min/max range; ignored for public files. Defaults to the server's configured expiry. (optional)

    try:
        # Get a download URL for a file
        api_response = api_instance.api_files_download_file_id_get(file_id, expires_in=expires_in)
        print("The response of FilesApi->api_files_download_file_id_get:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling FilesApi->api_files_download_file_id_get: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **file_id** | **str**|  | 
 **expires_in** | **int**| Signed-URL lifetime in seconds for private files. Clamped to the server&#39;s min/max range; ignored for public files. Defaults to the server&#39;s configured expiry. | [optional] 

### Return type

[**ApiFilesDownloadFileIdGet200Response**](ApiFilesDownloadFileIdGet200Response.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [ProjectBearerAuth](../README.md#ProjectBearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Download URL (signed for private files, permanent for public files) |  -  |
**403** | Access denied or download limit exceeded |  -  |
**404** | File not found |  -  |
**500** | Failed to generate download URL |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **api_files_logo_redirect_get**
> api_files_logo_redirect_get(key)

Redirect to an org/project logo's content

Unauthenticated. Logos are always meant to be public branding assets, but the object storage backend has no per-object ACL, so this route (not the bucket) is what actually serves them - the `key` query param is validated against the exact shape logoStorageService.uploadLogo() produces before signing, so this can never be used to fetch an arbitrary storage key. 302-redirects to a short-lived signed GET url.

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
    api_instance = mudbase.FilesApi(api_client)
    key = 'key_example' # str | 

    try:
        # Redirect to an org/project logo's content
        api_instance.api_files_logo_redirect_get(key)
    except Exception as e:
        print("Exception when calling FilesApi->api_files_logo_redirect_get: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **key** | **str**|  | 

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**302** | Redirect to a short-lived signed download URL |  -  |
**400** | Key does not match the expected logo key shape |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **api_files_public_file_id_get**
> api_files_public_file_id_get(file_id)

Redirect to a public file's content

Unauthenticated. Only serves files with isPublic=true whose upload has been confirmed and whose virus scan came back clean - the object storage backend has no per-object ACL, so this route (not the storage bucket) is what actually decides whether a "public" file's bytes are reachable. 302-redirects to a fresh, short-lived (60s) signed GET url so the actual bytes are still served straight off the storage edge.

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
    api_instance = mudbase.FilesApi(api_client)
    file_id = 'file_id_example' # str | 

    try:
        # Redirect to a public file's content
        api_instance.api_files_public_file_id_get(file_id)
    except Exception as e:
        print("Exception when calling FilesApi->api_files_public_file_id_get: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **file_id** | **str**|  | 

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**302** | Redirect to a short-lived signed download URL |  -  |
**403** | File is not public |  -  |
**404** | File not found, or not yet confirmed/scanned |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **confirm_direct_upload**
> ConfirmUploadResponse confirm_direct_upload(confirm_direct_upload_request)

Confirm direct upload (scan + finalize metadata)

After a client uploads directly to object storage using the presigned PUT URL, call this endpoint to have the server scan the object, create the File record, and optionally quarantine if infected.

### Example

* Api Key Authentication (ApiKeyAuth):
* Bearer (JWT) Authentication (ProjectBearerAuth):

```python
import mudbase
from mudbase.models.confirm_direct_upload_request import ConfirmDirectUploadRequest
from mudbase.models.confirm_upload_response import ConfirmUploadResponse
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

# Configure API key authorization: ApiKeyAuth
configuration.api_key['ApiKeyAuth'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['ApiKeyAuth'] = 'Bearer'

# Configure Bearer authorization (JWT): ProjectBearerAuth
configuration = mudbase.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with mudbase.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = mudbase.FilesApi(api_client)
    confirm_direct_upload_request = {"key":"65a1b2c3d4e5f6789012345a/default/abcd-1234-invoice.pdf","projectId":"65a1b2c3d4e5f6789012345a","originalName":"invoice.pdf","contentType":"application/pdf","size":52312,"isPublic":false} # ConfirmDirectUploadRequest | 

    try:
        # Confirm direct upload (scan + finalize metadata)
        api_response = api_instance.confirm_direct_upload(confirm_direct_upload_request)
        print("The response of FilesApi->confirm_direct_upload:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling FilesApi->confirm_direct_upload: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **confirm_direct_upload_request** | [**ConfirmDirectUploadRequest**](ConfirmDirectUploadRequest.md)|  | 

### Return type

[**ConfirmUploadResponse**](ConfirmUploadResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [ProjectBearerAuth](../README.md#ProjectBearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | File confirmed and metadata stored |  -  |
**400** | Bad request or file quarantined |  -  |
**401** | Authentication required |  -  |
**403** | Access denied |  -  |
**413** | File or request body exceeds plan single-upload limit (or platform ceiling) |  -  |
**429** | Rate limit exceeded |  -  |
**500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_file**
> MessageResponse delete_file(project_id, bucket_id, file_id)

Delete file

Delete a file from a bucket permanently.
Accepts: OrgBearerAuth (for admin users), ProjectBearerAuth (JWT for authenticated users), or ApiKeyAuth (X-API-Key for programmatic access). Both ProjectBearerAuth and ApiKeyAuth are fully implemented.


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
    api_instance = mudbase.FilesApi(api_client)
    project_id = 'project_id_example' # str | 
    bucket_id = 'bucket_id_example' # str | 
    file_id = 'file_id_example' # str | 

    try:
        # Delete file
        api_response = api_instance.delete_file(project_id, bucket_id, file_id)
        print("The response of FilesApi->delete_file:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling FilesApi->delete_file: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **str**|  | 
 **bucket_id** | **str**|  | 
 **file_id** | **str**|  | 

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
**200** | File deleted successfully |  -  |
**400** | Bad request |  -  |
**401** | Authentication required |  -  |
**403** | Access denied |  -  |
**409** | Resource conflict |  -  |
**429** | Rate limit exceeded |  -  |
**500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **download_bucket_file**
> bytearray download_bucket_file(file_id, token=token)

Download file from bucket

Download a file from a bucket. For public files, no authentication is required.
For private files, a download token (obtained via signed URL endpoint) is required in the query parameter.
Accepts: Token-based authentication via query parameter (for private files), or no authentication (for public files).


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
    api_instance = mudbase.FilesApi(api_client)
    file_id = '685af8b85d73a104065b6a77' # str | 
    token = 'token_example' # str |  (optional)

    try:
        # Download file from bucket
        api_response = api_instance.download_bucket_file(file_id, token=token)
        print("The response of FilesApi->download_bucket_file:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling FilesApi->download_bucket_file: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **file_id** | **str**|  | 
 **token** | **str**|  | [optional] 

### Return type

**bytearray**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/octet-stream, application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | File download |  * Content-Type -  <br>  * Content-Length -  <br>  * Content-Disposition -  <br>  |
**403** | Access denied or invalid token |  -  |
**404** | File not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **download_file**
> SignedUrlResponse download_file(file_id, token=token)

Generate a presigned URL for downloading a file

Returns a time-limited provider-signed URL for direct download. Server enforces RBAC before issuing the URL.

### Example

* Api Key Authentication (ApiKeyAuth):
* Bearer (JWT) Authentication (ProjectBearerAuth):

```python
import mudbase
from mudbase.models.signed_url_response import SignedUrlResponse
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

# Configure API key authorization: ApiKeyAuth
configuration.api_key['ApiKeyAuth'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['ApiKeyAuth'] = 'Bearer'

# Configure Bearer authorization (JWT): ProjectBearerAuth
configuration = mudbase.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with mudbase.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = mudbase.FilesApi(api_client)
    file_id = 'file_id_example' # str | 
    token = 'token_example' # str |  (optional)

    try:
        # Generate a presigned URL for downloading a file
        api_response = api_instance.download_file(file_id, token=token)
        print("The response of FilesApi->download_file:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling FilesApi->download_file: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **file_id** | **str**|  | 
 **token** | **str**|  | [optional] 

### Return type

[**SignedUrlResponse**](SignedUrlResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [ProjectBearerAuth](../README.md#ProjectBearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Signed URL generated |  -  |
**400** | Bad request |  -  |
**401** | Authentication required |  -  |
**403** | Access denied |  -  |
**409** | Resource conflict |  -  |
**429** | Rate limit exceeded |  -  |
**500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **generate_presigned_upload**
> PresignedPostResponse generate_presigned_upload(generate_presigned_upload_request)

Generate a presigned PUT URL for direct browser upload

Issue a presigned PUT URL for clients to upload directly to object storage. The server stores the issued key with expiry and RBAC is enforced.
PUT (not POST) is used because the object storage backend does not implement a POST-based upload API. The client must PUT the file body to `url` with the exact `headers` returned (a Content-Type mismatch fails with SignatureDoesNotMatch). `maxFileUploadBytes` is enforced server-side by `/api/files/upload/confirm` after the upload, not by the presigned URL itself.


### Example

* Api Key Authentication (ApiKeyAuth):
* Bearer (JWT) Authentication (ProjectBearerAuth):

```python
import mudbase
from mudbase.models.generate_presigned_upload_request import GeneratePresignedUploadRequest
from mudbase.models.presigned_post_response import PresignedPostResponse
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

# Configure API key authorization: ApiKeyAuth
configuration.api_key['ApiKeyAuth'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['ApiKeyAuth'] = 'Bearer'

# Configure Bearer authorization (JWT): ProjectBearerAuth
configuration = mudbase.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with mudbase.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = mudbase.FilesApi(api_client)
    generate_presigned_upload_request = {"projectId":"65a1b2c3d4e5f6789012345a","bucket":"default","originalName":"invoice.pdf","contentType":"application/pdf","isPublic":false} # GeneratePresignedUploadRequest | 

    try:
        # Generate a presigned PUT URL for direct browser upload
        api_response = api_instance.generate_presigned_upload(generate_presigned_upload_request)
        print("The response of FilesApi->generate_presigned_upload:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling FilesApi->generate_presigned_upload: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **generate_presigned_upload_request** | [**GeneratePresignedUploadRequest**](GeneratePresignedUploadRequest.md)|  | 

### Return type

[**PresignedPostResponse**](PresignedPostResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth), [ProjectBearerAuth](../README.md#ProjectBearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Presigned PUT URL |  -  |
**400** | Bad request |  -  |
**401** | Authentication required |  -  |
**403** | Access denied |  -  |
**429** | Rate limit exceeded |  -  |
**500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **generate_signed_url**
> SignedUrlResponse generate_signed_url(project_id, bucket_id, file_id, generate_signed_url_request=generate_signed_url_request)

Generate signed URL for file

Generate a time-limited signed URL for downloading a private file.
Accepts: OrgBearerAuth (for admin users), ProjectBearerAuth (JWT for authenticated users), or ApiKeyAuth (X-API-Key for programmatic access). Both ProjectBearerAuth and ApiKeyAuth are fully implemented.


### Example

* Bearer (JWT) Authentication (OrgBearerAuth):
* Api Key Authentication (ApiKeyAuth):
* Bearer (JWT) Authentication (ProjectBearerAuth):

```python
import mudbase
from mudbase.models.generate_signed_url_request import GenerateSignedUrlRequest
from mudbase.models.signed_url_response import SignedUrlResponse
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

# Configure API key authorization: ApiKeyAuth
configuration.api_key['ApiKeyAuth'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['ApiKeyAuth'] = 'Bearer'

# Configure Bearer authorization (JWT): ProjectBearerAuth
configuration = mudbase.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with mudbase.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = mudbase.FilesApi(api_client)
    project_id = 'project_id_example' # str | 
    bucket_id = 'bucket_id_example' # str | 
    file_id = 'file_id_example' # str | 
    generate_signed_url_request = {"expiresIn":3600} # GenerateSignedUrlRequest |  (optional)

    try:
        # Generate signed URL for file
        api_response = api_instance.generate_signed_url(project_id, bucket_id, file_id, generate_signed_url_request=generate_signed_url_request)
        print("The response of FilesApi->generate_signed_url:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling FilesApi->generate_signed_url: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **str**|  | 
 **bucket_id** | **str**|  | 
 **file_id** | **str**|  | 
 **generate_signed_url_request** | [**GenerateSignedUrlRequest**](GenerateSignedUrlRequest.md)|  | [optional] 

### Return type

[**SignedUrlResponse**](SignedUrlResponse.md)

### Authorization

[OrgBearerAuth](../README.md#OrgBearerAuth), [ApiKeyAuth](../README.md#ApiKeyAuth), [ProjectBearerAuth](../README.md#ProjectBearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Signed URL generated |  -  |
**400** | Bad request |  -  |
**401** | Authentication required |  -  |
**403** | Access denied |  -  |
**409** | Resource conflict |  -  |
**429** | Rate limit exceeded |  -  |
**500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_file**
> FileResponse get_file(project_id, bucket_id, file_id)

Get file metadata

Get metadata for a specific file in a bucket.
Accepts: OrgBearerAuth (for admin users), ProjectBearerAuth (JWT for authenticated users), or ApiKeyAuth (X-API-Key for programmatic access). Both ProjectBearerAuth and ApiKeyAuth are fully implemented.


### Example

* Bearer (JWT) Authentication (OrgBearerAuth):
* Api Key Authentication (ApiKeyAuth):
* Bearer (JWT) Authentication (ProjectBearerAuth):

```python
import mudbase
from mudbase.models.file_response import FileResponse
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

# Configure API key authorization: ApiKeyAuth
configuration.api_key['ApiKeyAuth'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['ApiKeyAuth'] = 'Bearer'

# Configure Bearer authorization (JWT): ProjectBearerAuth
configuration = mudbase.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with mudbase.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = mudbase.FilesApi(api_client)
    project_id = 'project_id_example' # str | 
    bucket_id = 'bucket_id_example' # str | 
    file_id = 'file_id_example' # str | 

    try:
        # Get file metadata
        api_response = api_instance.get_file(project_id, bucket_id, file_id)
        print("The response of FilesApi->get_file:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling FilesApi->get_file: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **str**|  | 
 **bucket_id** | **str**|  | 
 **file_id** | **str**|  | 

### Return type

[**FileResponse**](FileResponse.md)

### Authorization

[OrgBearerAuth](../README.md#OrgBearerAuth), [ApiKeyAuth](../README.md#ApiKeyAuth), [ProjectBearerAuth](../README.md#ProjectBearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | File metadata |  -  |
**400** | Bad request |  -  |
**401** | Authentication required |  -  |
**403** | Access denied |  -  |
**409** | Resource conflict |  -  |
**429** | Rate limit exceeded |  -  |
**500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_files**
> FileListResponse list_files(project_id, bucket_id, page=page, limit=limit, search=search, type=type)

List files in bucket

### Example

* Bearer (JWT) Authentication (OrgBearerAuth):
* Bearer (JWT) Authentication (ProjectBearerAuth):

```python
import mudbase
from mudbase.models.file_list_response import FileListResponse
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
    api_instance = mudbase.FilesApi(api_client)
    project_id = 'project_id_example' # str | 
    bucket_id = 'bucket_id_example' # str | 
    page = 1 # int |  (optional) (default to 1)
    limit = 20 # int |  (optional) (default to 20)
    search = 'search_example' # str |  (optional)
    type = 'type_example' # str |  (optional)

    try:
        # List files in bucket
        api_response = api_instance.list_files(project_id, bucket_id, page=page, limit=limit, search=search, type=type)
        print("The response of FilesApi->list_files:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling FilesApi->list_files: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **str**|  | 
 **bucket_id** | **str**|  | 
 **page** | **int**|  | [optional] [default to 1]
 **limit** | **int**|  | [optional] [default to 20]
 **search** | **str**|  | [optional] 
 **type** | **str**|  | [optional] 

### Return type

[**FileListResponse**](FileListResponse.md)

### Authorization

[OrgBearerAuth](../README.md#OrgBearerAuth), [ProjectBearerAuth](../README.md#ProjectBearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | List of files |  -  |
**400** | Bad request |  -  |
**401** | Authentication required |  -  |
**403** | Access denied |  -  |
**409** | Resource conflict |  -  |
**429** | Rate limit exceeded |  -  |
**500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **upload_files**
> FileUploadResponse upload_files(project_id, bucket_id, files)

Upload files to bucket

Upload one or more files to a storage bucket using multipart/form-data.
Per-file size is limited by the org plan (`maxFileUploadBytes`) and bucket `maxFileSize`, whichever is stricter. Exceeding the limit returns **413**.
Accepts: OrgBearerAuth (for admin users), ProjectBearerAuth (JWT for authenticated users), or ApiKeyAuth (X-API-Key for programmatic access). Both ProjectBearerAuth and ApiKeyAuth are fully implemented.


### Example

* Bearer (JWT) Authentication (OrgBearerAuth):
* Api Key Authentication (ApiKeyAuth):
* Bearer (JWT) Authentication (ProjectBearerAuth):

```python
import mudbase
from mudbase.models.file_upload_response import FileUploadResponse
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

# Configure API key authorization: ApiKeyAuth
configuration.api_key['ApiKeyAuth'] = os.environ["API_KEY"]

# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['ApiKeyAuth'] = 'Bearer'

# Configure Bearer authorization (JWT): ProjectBearerAuth
configuration = mudbase.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with mudbase.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = mudbase.FilesApi(api_client)
    project_id = 'project_id_example' # str | 
    bucket_id = 'bucket_id_example' # str | 
    files = None # List[bytearray] | 

    try:
        # Upload files to bucket
        api_response = api_instance.upload_files(project_id, bucket_id, files)
        print("The response of FilesApi->upload_files:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling FilesApi->upload_files: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **str**|  | 
 **bucket_id** | **str**|  | 
 **files** | **List[bytearray]**|  | 

### Return type

[**FileUploadResponse**](FileUploadResponse.md)

### Authorization

[OrgBearerAuth](../README.md#OrgBearerAuth), [ApiKeyAuth](../README.md#ApiKeyAuth), [ProjectBearerAuth](../README.md#ProjectBearerAuth)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | Files uploaded successfully |  -  |
**400** | Bad request |  -  |
**401** | Authentication required |  -  |
**403** | Access denied |  -  |
**409** | Resource conflict |  -  |
**413** | File or request body exceeds plan single-upload limit (or platform ceiling) |  -  |
**429** | Rate limit exceeded |  -  |
**500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

