# MUDBASE python SDK

Official **python** client for the [MUDBASE](https://mudbase.dev) platform.  
Packages are versioned from our OpenAPI spec so they stay in sync with the API.

## Installation

```bash
pip install mudbase
```

## Usage

```python
from mudbase import Client

client = Client(api_key="YOUR_API_KEY")
users = client.users.list()
```

## Documentation

- **Docs & API reference:** https://docs.mudbase.dev
- **Product:** https://mudbase.dev

## Support

Issues for this mirror repo: https://github.com/themudhaxk/mudbase-sdk-python
