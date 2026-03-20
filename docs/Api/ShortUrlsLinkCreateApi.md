# BSG\Api\V2\ShortUrlsLinkCreateApi

All URIs are relative to https://one-api.bsg.world, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**shortUrlsLinkCreate()**](ShortUrlsLinkCreateApi.md#shortUrlsLinkCreate) | **POST** /api/short-url/links | Create short link |


## `shortUrlsLinkCreate()`

```php
shortUrlsLinkCreate($link_store_request): \BSG\Api\V2\Model\ShortUrlsLinkCreate201Response
```

Create short link

Create a short link for original link.  **Please note:** *Response contains new link status. If original link is used at first time it may not pass the moderation automatically. Be careful only link in **active** status can be used for redirect!*

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: ExternalAuth
$config = BSG\Api\V2\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new BSG\Api\V2\Api\ShortUrlsLinkCreateApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$link_store_request = new \BSG\Api\V2\Model\LinkStoreRequest(); // \BSG\Api\V2\Model\LinkStoreRequest

try {
    $result = $apiInstance->shortUrlsLinkCreate($link_store_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ShortUrlsLinkCreateApi->shortUrlsLinkCreate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters


| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **link_store_request** | [**\BSG\Api\V2\Model\LinkStoreRequest**](../Model/LinkStoreRequest.md) |  | |

### Return type

[**\BSG\Api\V2\Model\ShortUrlsLinkCreate201Response**](../Model/ShortUrlsLinkCreate201Response.md)

### Authorization

[ExternalAuth](../../README.md#ExternalAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
