
# Sigmie HTTP Client

This is a simple HTTP client. It allows you to interact with the JSON APIs in a more convenient and efficient way.

## Installation

You can install the package via composer:

```bash
composer require sigmie/http
```

## Usage

Here is a basic example of how to use the client:

```php
use GuzzleHttp\Psr7\Uri;
use Sigmie\Http\Contracts\JSONResponse;
use Sigmie\Http\JSONClient;
use Sigmie\Http\JSONRequest;

$http = JSONClient::create(
    [
        "https://api.example.com/v1",
    ],
    [
        'connect_timeout' => 30 
    ]
);

$request = new JSONRequest('GET', new Uri('/campaigns'));

/** @var JSONResponse $response */
$response = $http->request($req);
```
