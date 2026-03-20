# BSG\Api\V2\ShortUrlsLinkApi

All URIs are relative to https://one-api.bsg.world, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**shortUrlsLink()**](ShortUrlsLinkApi.md#shortUrlsLink) | **GET** /api/short-url/links/{uuid}/statistics | Get short link statistic |


## `shortUrlsLink()`

```php
shortUrlsLink($uuid): \BSG\Api\V2\Model\ShortUrlsLink200Response
```

Get short link statistic

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: ExternalAuth
$config = BSG\Api\V2\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new BSG\Api\V2\Api\ShortUrlsLinkApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$uuid = 'uuid_example'; // string | Uuid of entity

try {
    $result = $apiInstance->shortUrlsLink($uuid);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ShortUrlsLinkApi->shortUrlsLink: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters


| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **uuid** | **string** | Uuid of entity | |

### Return type

[**\BSG\Api\V2\Model\ShortUrlsLink200Response**](../Model/ShortUrlsLink200Response.md)

### Authorization

[ExternalAuth](../../README.md#ExternalAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
