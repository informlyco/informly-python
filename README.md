# Informly Python Library

[![fern shield](https://img.shields.io/badge/%F0%9F%8C%BF-Built%20with%20Fern-brightgreen)](https://buildwithfern.com?utm_source=github&utm_medium=github&utm_campaign=readme&utm_source=Informly%2FPython)
[![pypi](https://img.shields.io/pypi/v/informly-sdk)](https://pypi.python.org/pypi/informly-sdk)

The Informly Python library provides convenient access to the Informly APIs from Python.

## Table of Contents

- [Documentation](#documentation)
- [Installation](#installation)
- [Usage](#usage)
- [Environments](#environments)
- [Async Client](#async-client)
- [Exception Handling](#exception-handling)
- [Advanced](#advanced)
  - [Access Raw Response Data](#access-raw-response-data)
  - [Retries](#retries)
  - [Timeouts](#timeouts)
  - [Custom Client](#custom-client)

## Documentation

API reference documentation is available [here](https://docs.informly.com/docs/api-reference).

## Installation

```sh
pip install informly-sdk
```

## Usage

Instantiate and use the client with the following:

```python
from informly-sdk import Informly

client = Informly(
    token="<token>",
)

client.contacts.create_contact()
```

## Environments

This SDK allows you to configure different environments for API requests.

```python
from informly-sdk import Informly
from informly-sdk.environment import InformlyEnvironment

client = Informly(
    environment=InformlyEnvironment.DEFAULT,
)
```

## Async Client

The SDK also exports an `async` client so that you can make non-blocking calls to our API. Note that if you are constructing an Async httpx client class to pass into this client, use `httpx.AsyncClient()` instead of `httpx.Client()` (e.g. for the `httpx_client` parameter of this client).

```python
import asyncio

from informly-sdk import AsyncInformly

client = AsyncInformly(
    token="<token>",
)


async def main() -> None:
    await client.contacts.create_contact()


asyncio.run(main())
```

## Exception Handling

When the API returns a non-success status code (4xx or 5xx response), a subclass of the following error
will be thrown.

```python
from informly-sdk.core.api_error import ApiError

try:
    client.contacts.create_contact(...)
except ApiError as e:
    print(e.status_code)
    print(e.body)
```

## Advanced

### Access Raw Response Data

The SDK provides access to raw response data, including headers, through the `.with_raw_response` property.
The `.with_raw_response` property returns a "raw" client that can be used to access the `.headers` and `.data` attributes.

```python
from informly-sdk import Informly

client = Informly(...)
response = client.contacts.with_raw_response.create_contact(...)
print(response.headers)  # access the response headers
print(response.status_code)  # access the response status code
print(response.data)  # access the underlying object
```

### Retries

The SDK is instrumented with automatic retries with exponential backoff. A request will be retried as long
as the request is deemed retryable and the number of retry attempts has not grown larger than the configured
retry limit (default: 2).

A request is deemed retryable when any of the following HTTP status codes is returned:

- [408](https://developer.mozilla.org/en-US/docs/Web/HTTP/Status/408) (Timeout)
- [429](https://developer.mozilla.org/en-US/docs/Web/HTTP/Status/429) (Too Many Requests)
- [5XX](https://developer.mozilla.org/en-US/docs/Web/HTTP/Status/500) (Internal Server Errors)

Use the `max_retries` request option to configure this behavior.

```python
client.contacts.create_contact(..., request_options={
    "max_retries": 1
})
```

### Timeouts

The SDK defaults to a 60 second timeout. You can configure this with a timeout option at the client or request level.

```python
from informly-sdk import Informly

client = Informly(..., timeout=20.0)

# Override timeout for a specific method
client.contacts.create_contact(..., request_options={
    "timeout_in_seconds": 1
})
```

### Custom Client

You can override the `httpx` client to customize it for your use-case. Some common use-cases include support for proxies
and transports.

```python
import httpx
from informly-sdk import Informly

client = Informly(
    ...,
    httpx_client=httpx.Client(
        proxy="http://my.test.proxy.example.com",
        transport=httpx.HTTPTransport(local_address="0.0.0.0"),
    ),
)
```

