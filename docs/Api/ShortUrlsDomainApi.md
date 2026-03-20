# BSG\Api\V2\ShortUrlsDomainApi

All URIs are relative to https://one-api.bsg.world, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**shortUrlsDomain()**](ShortUrlsDomainApi.md#shortUrlsDomain) | **GET** /api/short-url/domains/{uuid} | Get domain by uuid |


## `shortUrlsDomain()`

```php
shortUrlsDomain($uuid): \BSG\Api\V2\Model\ShortUrlsDomain200Response
```

Get domain by uuid

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: ExternalAuth
$config = BSG\Api\V2\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new BSG\Api\V2\Api\ShortUrlsDomainApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$uuid = 'db05af9e-107e-4ed6-b1ac-a373d90109c8'; //  string | Uuid of entity

try {
    $result = $apiInstance->shortUrlsDomain($uuid);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ShortUrlsDomainApi->shortUrlsDomain: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters


| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **uuid** | **string** | Uuid of entity | |

### Return type

[**\BSG\Api\V2\Model\ShortUrlsDomain200Response**](../Model/ShortUrlsDomain200Response.md)

### Authorization

[ExternalAuth](../../README.md#ExternalAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
