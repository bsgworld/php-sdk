# BSG\Api\V2\ShortUrlsDomainUpdateApi

All URIs are relative to https://one-api.bsg.world, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**shortUrlsDomainUpdate()**](ShortUrlsDomainUpdateApi.md#shortUrlsDomainUpdate) | **PUT** /api/short-url/domains/{uuid} | Update domain |


## `shortUrlsDomainUpdate()`

```php
shortUrlsDomainUpdate($uuid, $domain_update_request): \BSG\Api\V2\Model\ShortUrlsDomainUpdate200Response
```

Update domain

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: ExternalAuth
$config = BSG\Api\V2\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new BSG\Api\V2\Api\ShortUrlsDomainUpdateApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$uuid = 'uuid_example'; // string | Uuid of entity
$domain_update_request = new \BSG\Api\V2\Model\DomainUpdateRequest([
    'is_default' => true,
]);
try {
    $result = $apiInstance->shortUrlsDomainUpdate($uuid, $domain_update_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ShortUrlsDomainUpdateApi->shortUrlsDomainUpdate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters


| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **uuid** | **string** | Uuid of entity | |
| **domain_update_request** | [**\BSG\Api\V2\Model\DomainUpdateRequest**](../Model/DomainUpdateRequest.md) |  | |

### Return type

[**\BSG\Api\V2\Model\ShortUrlsDomainUpdate200Response**](../Model/ShortUrlsDomainUpdate200Response.md)

### Authorization

[ExternalAuth](../../README.md#ExternalAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
