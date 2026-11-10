# Mudbase Python SDK

Official **Python** client for [Mudbase](https://mudbase.dev) - the backend platform for modern apps.

Mudbase is a backend platform: authentication, a schema-driven database, file storage, serverless functions, webhooks, and real-time and transactional messaging behind one API. The Python SDK is a native Python client for that API, so you can manage users and organizations, define collections and query data, store and serve files, invoke functions, and configure webhooks without hand-rolling HTTP requests.

## Quickstart

Install the SDK, then sign up a user, insert and query a record, and upload a file in about five minutes. You need a project ID and a project API key from your Mudbase dashboard. Python 3.9 or newer.

```bash
pip install mudbase
```

Save this as `quickstart.py` and replace the placeholders. Email verification is required by default, so run it in two passes. Pass 1: run steps 1 and 2 (step 2 will fail on the placeholder token) and check your inbox for the verification email. Pass 2: paste the token from the link into step 2, delete step 1 (signing up twice with the same email fails), and run the whole file again.

```python
import time
from mudbase import (
    ApiClient, AuthenticationApi, BucketsApi, Configuration, CreateBucketRequest, DataApi, FilesApi,
    LoginLocalUserRequest, RegisterLocalUserRequest, VerifyEmailAuthRequest,
)

PROJECT_ID = "YOUR_PROJECT_ID"
COLLECTION_ID = "YOUR_COLLECTION_ID"
EMAIL = "you@your-inbox.example"  # an address you can read
PASSWORD = "a-strong-password-123"

configuration = Configuration(host="https://cloud.mudbase.dev")
configuration.api_key["ApiKeyAuth"] = "YOUR_PROJECT_KEY"  # sent as the X-API-Key header

with ApiClient(configuration) as api_client:
    auth = AuthenticationApi(api_client)
    data = DataApi(api_client)
    buckets = BucketsApi(api_client)
    files = FilesApi(api_client)

    # 1. Sign up. With verification on, the response has require_verification=True and no token.
    signup = auth.register_local_user(RegisterLocalUserRequest(
        email=EMAIL, password=PASSWORD, firstName="Ada", lastName="Lovelace", projectId=PROJECT_ID,
    ))
    print("require_verification:", signup.require_verification)

    # 2. Verify with the token from the email link (lost it? call auth.resend_verification_auth).
    auth.verify_email_auth(VerifyEmailAuthRequest(token="TOKEN_FROM_EMAIL_LINK", projectId=PROJECT_ID))

    # 3. Log in. Later calls send the user's token together with the project key.
    login = auth.login_local_user(LoginLocalUserRequest(email=EMAIL, password=PASSWORD, projectId=PROJECT_ID))
    configuration.access_token = login.token

    # 4. Insert and query one record. The collection must already exist, so create it in the dashboard first.
    data.create_data(PROJECT_ID, COLLECTION_ID, {"title": "Hello from the SDK"})
    found = data.list_data(PROJECT_ID, COLLECTION_ID, limit=5, filter='{"title": "Hello from the SDK"}')
    print("documents:", found)

    # 5. Create a bucket and upload one file into it.
    bucket = buckets.create_bucket(PROJECT_ID, CreateBucketRequest(name=f"quickstart-{int(time.time())}"))
    uploaded = files.upload_files(PROJECT_ID, bucket.bucket.id, [("hello.txt", b"hello world")])
    print("uploaded:", uploaded.file)
```

Full docs: [docs.mudbase.dev](https://docs.mudbase.dev).

<!-- TODO(quickstart, unverified): setup.py names the package "mudbase-sdk" while pyproject.toml names it "mudbase". `pip install mudbase` follows pyproject.toml; confirm the PyPI name before merging. Not run against a live project. -->

## What you can do

- **Authentication** - sign-up, sign-in, sessions, and API key management
- **Database** - schema-defined collections with typed CRUD and filtered queries
- **Storage** - buckets and file uploads and downloads
- **Realtime** - WebSocket events and live data subscriptions
- **Functions** - deploy and invoke serverless functions
- **Messaging** - transactional email, SMS, and push notifications
- **Webhooks** - configurable delivery with retry and logs
- **Roles & permissions** - project-level access control

## Links

- **Documentation:** https://docs.mudbase.dev
- **API reference:** https://docs.mudbase.dev/api
- **Dashboard:** https://console.mudbase.dev
- **Status:** https://status.mudbase.dev
- **Product:** https://mudbase.dev

## Support

Questions or issues: open one at https://github.com/themudhaxk/mudbase-sdk-python, or reach us at support@mudbase.dev.
