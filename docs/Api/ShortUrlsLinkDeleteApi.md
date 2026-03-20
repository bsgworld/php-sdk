# BSG\Api\V2\ShortUrlsLinkDeleteApi

All URIs are relative to https://one-api.bsg.world, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**shortUrlsLinkDelete()**](ShortUrlsLinkDeleteApi.md#shortUrlsLinkDelete) | **DELETE** /api/short-url/links/{uuid} | Remove short link |


## `shortUrlsLinkDelete()`

```php
shortUrlsLinkDelete($uuid): mixed
```

Remove short link

If short link is *active* it will be *deleted*. Next few days this action can be reverted and link may become *active* again. If short link already *blocked* or *deleted* it will be removed permanently.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: ExternalAuth
$config = BSG\Api\V2\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new BSG\Api\V2\Api\ShortUrlsLinkDeleteApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$uuid = 'uuid_example'; // string | Uuid of entity

try {
    $result = $apiInstance->shortUrlsLinkDelete($uuid);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ShortUrlsLinkDeleteApi->shortUrlsLinkDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters


| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **uuid** | **string** | Uuid of entity | |

### Return type

**mixed**

### Authorization

[ExternalAuth](../../README.md#ExternalAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
