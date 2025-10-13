# OpenAPI\Client\EchoApi

All URIs are relative to https://www/api/v1, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**callEcho()**](EchoApi.md#callEcho) | **POST** /echo | Echo test |


## `callEcho()`

```php
callEcho($body): string
```

Echo test

Receive the exact message you've sent

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: api_key
$config = new OpenAPI\Client\Configuration(['apiKey' => 'YOUR_API_KEY']);


$apiInstance = new OpenAPI\Client\Api\EchoApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = 'body_example'; // string | Echo payload

try {
    $result = $apiInstance->callEcho($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EchoApi->callEcho: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **body** | **string**| Echo payload | |

### Return type

**string**

### Authorization

[api_key](../../README.md#api_key)

### HTTP request headers

- **Content-Type**: `application/json`, `application/xml`
- **Accept**: `application/json`, `application/xml`, `text/csv`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
