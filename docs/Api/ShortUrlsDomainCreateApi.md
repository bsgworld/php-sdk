# BSG\Api\V2\ShortUrlsDomainCreateApi

All URIs are relative to https://one-api.bsg.world, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**shortUrlsDomainCreate()**](ShortUrlsDomainCreateApi.md#shortUrlsDomainCreate) | **POST** /api/short-url/domains | Add domain |


## `shortUrlsDomainCreate()`

```php
shortUrlsDomainCreate($domain_store_request): \BSG\Api\V2\Model\ShortUrlsDomainCreate201Response
```

Add domain

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: ExternalAuth
$config = BSG\Api\V2\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new BSG\Api\V2\Api\ShortUrlsDomainCreateApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$domain_store_request = new \BSG\Api\V2\Model\DomainStoreRequest([
    'name' => 'short.ai',
    'slug_type' => 'random',
]);
try {
    $result = $apiInstance->shortUrlsDomainCreate($domain_store_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ShortUrlsDomainCreateApi->shortUrlsDomainCreate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters


| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **domain_store_request** | [**\BSG\Api\V2\Model\DomainStoreRequest**](../Model/DomainStoreRequest.md) |  | [optional] |

### Return type

[**\BSG\Api\V2\Model\ShortUrlsDomainCreate201Response**](../Model/ShortUrlsDomainCreate201Response.md)

### Authorization

[ExternalAuth](../../README.md#ExternalAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
